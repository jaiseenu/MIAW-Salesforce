<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
</head>
<body>
  <script type="text/javascript">
    async function getVisitorDetails() {
      const visitor = {
        transaction_id: "test_trans",
        lead_id: "test_lead",
        application_id: "test_appid",
        application_channel: "test_appchannel",
        page_info: "test_page",
        device_info: "test_device"
      };
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
            Transaction_ID: visitor.transaction_id,
            Lead_ID: visitor.lead_id,
            Application_ID: visitor.application_id,
            Application_Channel: visitor.application_channel,
            Page_Info: visitor.page_info,
            Device_Type: visitor.device_info
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
