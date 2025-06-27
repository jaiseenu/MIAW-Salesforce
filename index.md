<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
   </head>
   <body>
      <script type='text/javascript'>
         function getDeviceInfo() {
         const ua = navigator.userAgent;
         // For mobile devices
         if (/android/i.test(ua)) {
         const match = ua.match(/Android\s[\d\.]+;\s(.+?)\sBuild/);
         return match ? `Android Device: ${match[1]}` : "Android Device";
         }
         if (/iPhone/i.test(ua)) {
         return "Apple iPhone";
         }
         if (/iPad/i.test(ua)) {
         return "Apple iPad";
         }
         if (/Macintosh/i.test(ua)) {
         return "Mac Desktop";
         }
         if (/Windows/i.test(ua)) {
         return "Windows PC";
         }
         return "Unknown Device";
         }
         
         
         function initEmbeddedMessaging() {
         	try {
			
                        console.log('getDeviceInfo:##',getDeviceInfo());
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
