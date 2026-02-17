<!DOCTYPE html>
<html lang="en">
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
  <!-- DUMMY INPUTS FOR TESTING - START -->
  <style>
    .user-info-form {
      max-width: 400px;
      margin: 20px;
      padding: 20px;
      border: 1px solid #ddd;
      border-radius: 8px;
    }
    .form-group { margin-bottom: 15px; }
    label { display: block; margin-bottom: 5px; font-weight: bold; }
    input {
      width: 100%;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
    }
  </style>
</head>
<body>
<div class="user-info-form">
  <h3>User Information</h3>
  <div class="form-group">
    <label for="firstName">First Name:</label>
    <input type="text" id="firstName" placeholder="Enter first name">
  </div>
  <div class="form-group">
    <label for="lastName">Last Name:</label>
    <input type="text" id="lastName" placeholder="Enter last name">
  </div>
  <div class="form-group">
    <label for="email">Email:</label>
    <input type="email" id="email" placeholder="Enter email">
  </div>
</div>
<!-- DUMMY INPUTS FOR TESTING - END -->

<script>
  //replace the customer details such as first name, last name and email
  function getInputValues() {
    return {
      firstName: document.getElementById('firstName')?.value || '',
      lastName: document.getElementById('lastName')?.value || '',
      email: document.getElementById('email')?.value || ''
    };
  }

  //pass the values with the actual ones
  function getDetails() {
    return {
      Transaction_ID: "test_trans",
      Lead_ID: "test_lead",
      Application_ID: "test_appid",
      Application_Channel: "test_appchannel",
      Application_Error_Info: "test_error info",
      Page_Info: "test_page",
      Device_Type: "test_device"
    };
  }

  function initEmbeddedMessaging() {
    try {
      embeddedservice_bootstrap.settings.language = 'en_US';
      embeddedservice_bootstrap.init(
        '00Dce000001LoFm',
        'Web_Chat',
        'https://pflms--qa.sandbox.my.site.com/ESWWebChat1739454676991',
        { scrt2URL: 'https://pflms--qa.sandbox.my.salesforce-scrt.com' }
      );

      window.addEventListener("onEmbeddedMessagingButtonClicked", () => {
        console.log("Chat Button Clicked");
        embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields(getDetails());
        const inputValues = getInputValues();
        const isEditable = (value) => !value || value.trim() === "";
        embeddedservice_bootstrap.prechatAPI.setVisiblePrechatFields({
            "_firstName": {
                value: inputValues.firstName || "",
                isEditableByEndUser: isEditable(inputValues.firstName)
            },
            "_lastName": {
                value: inputValues.lastName || "",
                isEditableByEndUser: isEditable(inputValues.lastName)
            },
            "_email": {
                value: inputValues.email || "",
                isEditableByEndUser: isEditable(inputValues.email)
            }
        });
      });
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
