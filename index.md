<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
</head>
<body>
  <!-- First define the function -->
  <script type="text/javascript">
    function getDetails() {
      const visitor = {
        Transaction_ID: "test_trans",
        Lead_ID: "test_lead",
        Application_ID: "test_appid",
        Application_Channel: "test_appchannel",
        Page_Info: "test_page",
        Device_Type: "test_device"
      };
      return visitor;
    }

    async function initEmbeddedMessaging() {
      try {
        const visitor = getDetails();
        console.log("Visitor Details:", visitor);

        embeddedservice_bootstrap.settings.language = 'en_US';

        window.addEventListener("onEmbeddedMessagingReady", () => {
          console.log("onEmbeddedMessagingReady event received");
          embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields(getDetails());
        });

        window.addEventListener("onEmbeddedMessagingButtonClicked", () => {
          console.log("onEmbeddedMessagingButtonClicked event received");
          embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields(getDetails());

          if(visitor.Device_Type != ''){
            const success = embeddedservice_bootstrap.utilAPI.launchChat(); // Removed await
            console.log("LAUNCH SUCCESS:", success);
          }
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

  <!-- Then load the script that calls it -->
  <script
    src="https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991/assets/js/bootstrap.min.js"
    onload="initEmbeddedMessaging()">
  </script>
</body>
</html>
