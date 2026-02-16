<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
</head>
<body>
  <script type="text/javascript">
    async function getDetails() {
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
        const visitor = await getDetails();
        console.log("Visitor Details:", visitor);

        embeddedservice_bootstrap.settings.language = 'en_US';

        window.addEventListener("onEmbeddedMessagingReady", () => {
          console.log("onEmbeddedMessagingReady event received");

          // NOTE: The following field names (e.g., IP_Address, Referring_Site, etc.) 
          // must not be changed during assignment. These names must match 
          // exactly what is configured in Salesforce pre-chat mapping.
          embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields(getDetails());
        });

        // When user manually clicks the chat button
        window.addEventListener("onEmbeddedMessagingButtonClicked", () => {
          console.log("onEmbeddedMessagingButtonClicked event received");
          embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields(getDetails());

          if(visitor.Device_Type != ''){
            const success = await embeddedservice_bootstrap.utilAPI.launchChat();
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

  <script
    src="https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991/assets/js/bootstrap.min.js"
    onload="initEmbeddedMessaging()">
  </script>
</body>
</html>
