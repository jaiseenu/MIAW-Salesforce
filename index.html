<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
  <!-- Add some basic styling for the input fields -->
  <style>
    .user-info-form {
      max-width: 400px;
      margin: 20px;
      padding: 20px;
      border: 1px solid #ddd;
      border-radius: 8px;
    }
    .form-group {
      margin-bottom: 15px;
    }
    label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }
    input {
      width: 100%;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
    }
    button {
      background-color: #0070d2;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
    }
    button:hover {
      background-color: #005fb2;
    }
  </style>
</head>
<body>
  <!-- Add input fields for user information -->
  <div class="user-info-form">
    <h3>User Information</h3>
    <div class="form-group">
      <label for="firstName">First Name:</label>
      <input type="text" id="firstName" placeholder="Enter first name" value="Jane">
    </div>
    <div class="form-group">
      <label for="lastName">Last Name:</label>
      <input type="text" id="lastName" placeholder="Enter last name" value="A2">
    </div>
    <div class="form-group">
      <label for="email">Email:</label>
      <input type="email" id="email" placeholder="Enter email" value="test@sf.com">
    </div>
  </div>

  <!-- First define the function (exactly as original) -->
  <script type="text/javascript">

    function getInputValues() {
      return {
        firstName: document.getElementById('firstName')?.value || '',
        lastName: document.getElementById('lastName')?.value || '',
        email: document.getElementById('email')?.value || ''
      };
    }
    
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

       // window.addEventListener("onEmbeddedMessagingReady", () => {
       //   console.log("onEmbeddedMessagingReady event received");
      //    embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields(getDetails());
      //  });

        window.addEventListener("onEmbeddedMessagingButtonClicked", () => {
          console.log("onEmbeddedMessagingButtonClicked event received");
          embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields(getDetails());
          const inputValues = getInputValues();
          console.log("inputValues:", inputValues);
          embeddedservice_bootstrap.prechatAPI.setVisiblePrechatFields({
                   "_firstName": {
                      "value": inputValues.firstName,
                      "isEditableByEndUser": false
                    },
                    "_lastName": {
                      "value": inputValues.firstName,
                      "isEditableByEndUser": false
                    },
                    "_email": {
                      "value": inputValues.firstName,
                      "isEditableByEndUser": true
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
