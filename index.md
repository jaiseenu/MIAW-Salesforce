<html>
<body>
<button id="myButton">Click Me</button>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			console.log('::$$::', embeddedservice_bootstrap);
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00Dce000001LoFm',
				'Web_Chat',
				'https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991',
				{
					scrt2URL: 'https://pflms--qa.sandbox.my.salesforce-scrt.com'
				}
			);
			hideNotificationArea();
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};

	document.addEventListener('DOMContentLoaded', function() {
      hideNotificationArea();
    });

	function hideNotificationArea(){
		try {
			const chatElement = document.getElementById('embedded-messaging');
                        console.log('::$$chatElement::', chatElement);
                        const dd = document.getElementById('embeddedMessagingSiteContextFrame');
                        console.log('::$$dd::', dd);
                        // Add event listener
                       chatElement.addEventListener('click', function() {
                             alert('Button clicked! Heading says: ' , chatElement);
                       });
			
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};


document.getElementById('myButton').addEventListener('click', function() {
      hideNotificationArea();
    });
</script>
<script type='text/javascript' src='https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

</body>
</html>
