<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
   </head>
   <body>
      <script type='text/javascript'>
         
         async function getVisitorDetails(){
		const referringSite = document.referrer || "";
		const browserLanguage = navigator.language || "";
		const platform = navigator.platform || "";
		const screenResolution = `${screen.width} x ${screen.height}`;
		const userAgent = navigator.userAgent || "";
		let ipAddress = data.ip;
		let city = "";
		let region = "";
		let regionCode = "";
		let country = "";
		let countryCode = "";
		let network = "";
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
		} catch (error) {
			console.error("Error fetching visitor info:", error);
		}
		const visitorInfo = { ipAddress, city, region, regionCode, country, countryCode, network, referringSite,
			          browserLanguage, platform, screenResolution, userAgent };
		return visitorInfo;
	 }
         
         function initEmbeddedMessaging() {
         	try {
			const visitor_details = getVisitorDetails();
			console.log('VISITOR DETAILS:##', visitor_details);
         		console.log('embeddedservice_bootstrap:##', embeddedservice_bootstrap);
         		embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
         		//embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({"device" : "mobile!!"});
         window.addEventListener("onEmbeddedMessagingReady", () => {
         console.log("Received the onEmbeddedMessagingReady event…");
         embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({"device" : "mobile!!"});
         
         });
         console.log('embeddedservice_bootstrap:#2#', embeddedservice_bootstrap);
         		embeddedservice_bootstrap.init(
         			'00Dce000001LoFm',
         			'Web_Chat',
         			'https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991',
         			{
         				scrt2URL: 'https://pflms--qa.sandbox.my.salesforce-scrt.com'
         			}
         		);
         		
         	} catch (err) {
         		console.error('Error loading Embedded Messaging: ', err);
         	}
         };
      </script>
      <script type='text/javascript' src='https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
   </body>
</html>
