<html>

<body>
    <script type="text/javascript">
    document.addEventListener("DOMContentLoaded", function () {
        function initEmbeddedMessaging() {
            try {
                embeddedservice_bootstrap.settings.language = "en_US"; // Set language
                
                embeddedservice_bootstrap.init(
                    "00DcZ000000xcMD",  // Your Salesforce Org ID
                    "Web_Chat_v2",      // Your Deployment Name
                    "https://pflms--scvoicenew.sandbox.my.site.com/ESWWebChatv21737707144466",  // Your Chat Endpoint
                    {
                        scrt2URL: "https://pflms--scvoicenew.sandbox.my.salesforce-scrt.com"  // Secure URL
                    }
                );
            } catch (err) {
                console.error("Error loading Embedded Messaging: ", err);
            }
        }

        // Load the Embedded Service Bootstrap JS
        let script = document.createElement("script");
        script.src = "https://pflms--scvoicenew.sandbox.my.site.com/ESWWebChatv21737707144466/assets/js/bootstrap.min.js";
        script.onload = initEmbeddedMessaging;
        document.body.appendChild(script);
    });
</script>

</body>

</html>
