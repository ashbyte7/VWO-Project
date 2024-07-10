<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VWO Login Page Testing</title>
</head>
<body>
    <h1>VWO Login Page Testing</h1>

    <h2>Description</h2>
    <p>This project involves comprehensive testing of a VWO login page. The tests are designed to validate the functionality, security, and performance of the login page. The testing process includes creating and executing test cases, reporting bugs using Jira, and automating tests using Selenium with Python.</p>

    <h2>Features</h2>
    <ul>
        <li>Comprehensive Test Cases: Detailed test cases covering various scenarios for the login page.</li>
        <li>Automated Testing: Use of Selenium with Python to automate the testing process.</li>
        <li>Bug Reporting: Integration with Jira for efficient bug tracking and reporting.</li>
    </ul>

    <h2>Test Cases</h2>
    <table>
        <thead>
            <tr>
                <th>Scenario ID</th>
                <th>Scenario Description</th>
                <th>Test Case ID</th>
                <th>Test Case Title</th>
                <th>Pre Condition</th>
                <th>Steps to Execute</th>
                <th>Expected Result</th>
                <th>Actual Result</th>
                <th>Status</th>
                <th>Executed QA Name</th>
                <th>Comments</th>
                <th>Priority</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>SC-001</td>
                <td>Verify successful login with valid credentials</td>
                <td>TC-001</td>
                <td>Valid Login</td>
                <td>User has valid registered credentials.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Enter valid username/email.<br>3. Enter valid password.<br>4. Click on "Login".</td>
                <td>User should be successfully logged in and redirected to the dashboard.</td>
                <td>User successfully logged in and redirected to the dashboard.</td>
                <td>PASS</td>
                <td>Ashutosh</td>
                <td></td>
                <td>High</td>
            </tr>
            <tr>
                <td>SC-002</td>
                <td>Verify login with invalid password</td>
                <td>TC-002</td>
                <td>Invalid Password Login</td>
                <td>User has a registered username/email.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Enter valid username/email.<br>3. Enter invalid password.<br>4. Click on "Login".</td>
                <td>An error message should be displayed indicating incorrect password.</td>
                <td>Error message displayed "Your email, password, IP address or location did not match".</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>High</td>
            </tr>
            <tr>
                <td>SC-003</td>
                <td>Verify login with non-registered email</td>
                <td>TC-003</td>
                <td>Non-registered Email Login</td>
                <td>User should be on the login page.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Enter non-registered email.<br>3. Enter any password.<br>4. Click on "Login".</td>
                <td>An error message should be displayed indicating the email is not registered.</td>
                <td>Error message displayed "Your email, password, IP address or location did not match".</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>Medium</td>
            </tr>
            <tr>
                <td>SC-004</td>
                <td>Validate empty email field during login</td>
                <td>TC-004</td>
                <td>Empty Email Field</td>
                <td>User should be on the login page.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Leave the email field empty.<br>3. Enter any password.<br>4. Click on "Login".</td>
                <td>An error message should be displayed indicating the email field is required.</td>
                <td>Error message displayed "Your email, password, IP address or location did not match".</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>Medium</td>
            </tr>
            <tr>
                <td>SC-005</td>
                <td>Validate empty password field during login</td>
                <td>TC-005</td>
                <td>Empty Password Field</td>
                <td>User should be on the login page.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Enter valid username/email.<br>3. Leave the password field empty.<br>4. Click on "Login".</td>
                <td>An error message should be displayed indicating the password field is required.</td>
                <td>Error message displayed "Your email, password, IP address or location did not match".</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>Medium</td>
            </tr>
            <tr>
                <td>SC-006</td>
                <td>Verify login with case-sensitive password</td>
                <td>TC-006</td>
                <td>Case-sensitive Password</td>
                <td>User has a registered username/email and password with specific case sensitivity.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Enter valid username/email.<br>3. Enter password with incorrect case sensitivity.<br>4. Click on "Login".</td>
                <td>An error message should be displayed indicating incorrect password.</td>
                <td>Error message displayed "Your email, password, IP address or location did not match".</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>Medium</td>
            </tr>
            <tr>
                <td>SC-007</td>
                <td>Verify "Forgot Password" functionality</td>
                <td>TC-007</td>
                <td>Forgot Password Link</td>
                <td>User has a registered email.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Click on "Forgot Password".<br>3. Enter registered email.<br>4. Follow email instructions.</td>
                <td>Password reset email should be sent to the registered email address.</td>
                <td>Password reset email is sent to the registered email address.</td>
                <td>PASS</td>
                <td>Ashutosh</td>
                <td></td>
                <td>High</td>
            </tr>
            <tr>
                <td>SC-008</td>
                <td>Verify session timeout after login</td>
                <td>TC-008</td>
                <td>Session Timeout</td>
                <td>User is logged in to the application.</td>
                <td>1. Log in to "https://app.vwo.com/#/login".<br>2. Wait for the session timeout duration (e.g., 15 minutes of inactivity).</td>
                <td>User should be prompted to log in again after session timeout.</td>
                <td>Session timeout did not occur as expected. The user remained logged in without being prompted to log in again.</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>Medium</td>
            </tr>
            <tr>
                <td>SC-009</td>
                <td>Verify concurrent login restriction</td>
                <td>TC-009</td>
                <td>Concurrent Login Restriction</td>
                <td>User has valid registered credentials.</td>
                <td>1. Log in to "https://app.vwo.com/#/login" on Browser 1.<br>2. Attempt to log in to the same account on Browser 2 simultaneously.</td>
                <td>The application should restrict concurrent login and display a message indicating restriction.</td>
                <td>The application allowed concurrent logins from both browsers simultaneously without restricting access or displaying any message indicating a restriction.</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>Medium</td>
            </tr>
            <tr>
                <td>SC-010</td

>
                <td>Verify brute force attack prevention</td>
                <td>TC-010</td>
                <td>Brute Force Attack Prevention</td>
                <td>User should be on the login page.</td>
                <td>1. Navigate to "https://app.vwo.com/#/login".<br>2. Attempt to log in with invalid credentials multiple times (e.g., more than 5 attempts).</td>
                <td>After a threshold, the account should be locked, or a delay should be enforced.</td>
                <td>A captcha box appeared, but the login functionality continued to work as before without any account locking or enforced delay.</td>
                <td>FAIL</td>
                <td>Ashutosh</td>
                <td></td>
                <td>High</td>
            </tr>
        </tbody>
    </table>


    <h2>Acknowledgements</h2>
    <ul>
        <li><a href="https://www.selenium.dev/">Selenium</a></li>
        <li><a href="https://www.python.org/">Python</a></li>
        <li><a href="https://www.atlassian.com/software/jira">Jira</a></li>
    </ul>
</body>
</html>
