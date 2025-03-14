<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Secure Form</title>
    <meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self'; style-src 'self'">
</head>
<body>
    <h1>Secure Form</h1>
    <p>Always use HTTPS for secure communication.</p>

    <form id="myForm" action="/submit" method="post">
        <input type="hidden" id="csrf_token" name="csrf_token" value="exampleToken">
        <label for="username">Username:</label><br>
        <input type="text" id="username" name="username" required><br><br>

        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" required><br><br>

        <label for="password">Password:</label><br>
        <input type="password" id="password" name="password" required><br><br>

        <input type="submit" value="Submit">
    </form>

    <script>
        // Client-side input validation example (more robust validation should be done server-side)
        document.getElementById('myForm').addEventListener('submit', function(event) {
            const username = document.getElementById('username').value;
            if (username.length < 3) {
                alert('Username must be at least 3 characters long.');
                event.preventDefault(); // Prevent form submission
            }
        });
    </script>
</body>
</html>
# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.
