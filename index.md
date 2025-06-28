<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
</head>
<body>
  <script type="text/javascript">
    async function getVisitorDetails() {
      // Basic client-side details
      const referringSite = document.referrer || "";
      const browserLanguage = navigator.language || "";
      const platform = navigator.platform || "";
      const screenResolution = `${screen.width} x ${screen.height}`;
      const userAgent = navigator.userAgent || "";

      // Initialize IP-based details
      let ipAddress = "", city = "", region = "", regionCode = "";
      let country = "", countryCode = "", network = "", timezone = "";

      try {
        const response = await fetch('https://ipapi.co/json/');
        const data = await response.json();

        ipAddress = data.ip;
        city = data.city;
        region = data.region;
        regionCode = data.region_code;
        country = data.country_name;
        countryCode = data.country_code;
        network = data.org;
        timezone = data.timezone;
      } catch (error) {
        console.error("Error fetching visitor info:", error);
      }
      
      let locationParts = [];
      if (city) locationParts.push(city);
      if (regionCode) locationParts.push(regionCode);
      if (country) locationParts.push(country);
      
      const location = locationParts.join(", ");
      return {
        ipAddress, city, region, regionCode, country, countryCode, location, network, timezone,
        referringSite, browserLanguage, platform, screenResolution, userAgent
      };
    }

    async function initEmbeddedMessaging() {
      try {
        const visitorDetails = await getVisitorDetails();
        console.log("VISITOR DETAILS:", visitorDetails);
        console.log("embeddedservice_bootstrap:", embeddedservice_bootstrap);

        embeddedservice_bootstrap.settings.language = 'en_US';

        // Optional: detect device type
        const isMobile = /Mobi|Android/i.test(navigator.userAgent);
        const deviceType = isMobile ? "Mobile" : "Desktop";

        window.addEventListener("onEmbeddedMessagingReady", () => {
          console.log("Received the onEmbeddedMessagingReady event…");
          embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({
            device: deviceType,
            IP_Address: visitorDetails.ipAddress,
            Referring_Site: visitorDetails.referringSite,
            Network: visitorDetails.network,
            Browser_Language: visitorDetails.browserLanguage,
            Platform: visitorDetails.platform,
            Screen_Resolution: visitorDetails.screenResolution,
            User_Agent: visitorDetails.userAgent,
            Location: visitorDetails.location,
            Timezone: visitorDetails.timezone
          });
        });

        embeddedservice_bootstrap.init(
          '00Dce000001LoFm',
          'Web_Chat',
          'https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991',
          {
            scrt2URL: 'https://pflms--qa.sandbox.my.salesforce-scrt.com'
          }
        );

      } catch (err) {
        console.error("Error initializing Embedded Messaging:", err);
      }
    }
  </script>

  <script
    type="text/javascript"
    src="https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991/assets/js/bootstrap.min.js"
    onload="initEmbeddedMessaging()">
  </script>
</body>
</html>
