<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
</head>
<body>
  <script type="text/javascript">
    async function getVisitorDetails() {
      const visitor = {
        referringSite: document.referrer || "",
        browserLanguage: navigator.language || "",
        platform: navigator.platform || "",
        screenResolution: `${screen.width} x ${screen.height}`,
        userAgent: navigator.userAgent || ""
      };

      try {
        const response = await fetch('https://ipapi.co/json/');
        if (!response.ok) throw new Error("Failed to fetch IP data");
        const data = await response.json();

        visitor.ipAddress = data.ip || "";
        visitor.city = data.city || "";
        visitor.region = data.region || "";
        visitor.regionCode = data.region_code || "";
        visitor.country = data.country_name || "";
        visitor.countryCode = data.country_code || "";
        visitor.network = data.org || "";
        visitor.timezone = data.timezone || "";

        const locationParts = [visitor.city, visitor.regionCode, visitor.country].filter(Boolean);
        visitor.location = locationParts.join(", ");

      } catch (error) {
        console.error("Error fetching visitor info:", error);
      }

      return visitor;
    }

    async function initEmbeddedMessaging() {
      try {
        const visitor = await getVisitorDetails();
        console.log("Visitor Details:", visitor);

        embeddedservice_bootstrap.settings.language = 'en_US';

        window.addEventListener("onEmbeddedMessagingReady", () => {
          console.log("onEmbeddedMessagingReady event received");

          // NOTE: The following field names (e.g., IP_Address, Referring_Site, etc.) 
          // must not be changed during assignment. These names must match 
          // exactly what is configured in Salesforce pre-chat mapping.
          embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({
            IP_Address: visitor.ipAddress,
            Referring_Site: visitor.referringSite,
            Network: visitor.network,
            Browser_Language: visitor.browserLanguage,
            Platform: visitor.platform,
            Screen_Resolution: visitor.screenResolution,
            User_Agent: visitor.userAgent,
            Location: visitor.location,
            Timezone: visitor.timezone
          });
        });

        embeddedservice_bootstrap.init(
          '00Dce000001LoFm',
          'Web_Chat',
          'https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991',
          { scrt2URL: 'https://pflms--qa.sandbox.my.salesforce-scrt.com' }
        );

      } catch (error) {
        console.error("Error initializing Embedded Messaging:", error);
      }
    }
  </script>

  <script
    src="https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991/assets/js/bootstrap.min.js"
    onload="initEmbeddedMessaging()">
  </script>
</body>
</html>
