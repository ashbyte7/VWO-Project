
# VWO Login Page Testing

## Description

This project involves comprehensive testing of a VWO login page. The tests are designed to validate the functionality, security, and performance of the login page. The testing process includes creating and executing test cases, reporting bugs using Jira, and automating tests using Selenium with Python.

## Features

- **Comprehensive Test Cases**: Detailed test cases covering various scenarios for the login page.
- **Automated Testing**: Use of Selenium with Python to automate the testing process.
- **Bug Reporting**: Integration with Jira for efficient bug tracking and reporting.

## Prerequisites

Before running the tests, ensure you have the following installed and set up:

- Windows 11
- Python 3.x
- Selenium WebDriver
- Jira account (for bug reporting)

## Test Cases

- **Scenario 1: Verify successful login with valid credentials**
  - User has valid registered credentials.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Enter valid username/email.
    3. Enter valid password.
    4. Click on "Login".
  - Expected Result: User should be successfully logged in and redirected to the dashboard.
  - Actual Result: User successfully logged in and redirected to the dashboard.
  - Status: PASS

- **Scenario 2: Verify login with invalid password**
  - User has a registered username/email.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Enter valid username/email.
    3. Enter invalid password.
    4. Click on "Login".
  - Expected Result: An error message should be displayed indicating incorrect password.
  - Actual Result: Error message displayed "Your email, password, IP address or location did not match".
  - Status: FAIL

- **Scenario 3: Verify login with non-registered email**
  - User should be on the login page.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Enter non-registered email.
    3. Enter any password.
    4. Click on "Login".
  - Expected Result: An error message should be displayed indicating the email is not registered.
  - Actual Result: Error message displayed "Your email, password, IP address or location did not match".
  - Status: FAIL

- **Scenario 4: Validate empty email field during login**
  - User should be on the login page.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Leave the email field empty.
    3. Enter any password.
    4. Click on "Login".
  - Expected Result: An error message should be displayed indicating the email field is required.
  - Actual Result: Error message displayed "Your email, password, IP address or location did not match".
  - Status: FAIL

- **Scenario 5: Validate empty password field during login**
  - User should be on the login page.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Enter valid username/email.
    3. Leave the password field empty.
    4. Click on "Login".
  - Expected Result: An error message should be displayed indicating the password field is required.
  - Actual Result: Error message displayed "Your email, password, IP address or location did not match".
  - Status: FAIL

- **Scenario 6: Verify login with case-sensitive password**
  - User has a registered username/email and password with specific case sensitivity.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Enter valid username/email.
    3. Enter password with incorrect case sensitivity.
    4. Click on "Login".
  - Expected Result: An error message should be displayed indicating incorrect password.
  - Actual Result: Error message displayed "Your email, password, IP address or location did not match".
  - Status: FAIL

- **Scenario 7: Verify "Forgot Password" functionality**
  - User has a registered email.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Click on "Forgot Password".
    3. Enter registered email.
    4. Follow email instructions.
  - Expected Result: Password reset email should be sent to the registered email address.
  - Actual Result: Password reset email is sent to the registered email address.
  - Status: PASS

 ** Scenario 8: Verify session timeout after login**
  - User is logged in to the application.
  - Steps:
    1. Log in to "https://app.vwo.com/#/login".
    2. Wait for the session timeout duration (e.g., 15 minutes of inactivity).
  - Expected Result: User should be prompted to log in again after session timeout.
  - Actual Result: Session timeout did not occur as expected. The user remained logged in without being prompted to log in again.
  - Status: FAIL

 ** Scenario 9: Verify concurrent login restriction**
  - User has valid registered credentials.
  - Steps:
    1. Log in to "https://app.vwo.com/#/login" on Browser 1.
    2. Attempt to log in to the same account on Browser 2 simultaneously.
  - Expected Result: The application should restrict concurrent login and display a message indicating restriction.
  - Actual Result: The application allowed concurrent logins from both browsers simultaneously without restricting access or displaying any message indicating a restriction.
  - Status: FAIL

  **Scenario 10: Verify brute force attack prevention**
  - User should be on the login page.
  - Steps:
    1. Navigate to "https://app.vwo.com/#/login".
    2. Attempt to log in with invalid credentials multiple times (e.g., more than 5 attempts).
  - Expected Result: After a threshold, the account should be locked, or a delay should be enforced.
  - Actual Result: A captcha box appeared, but the login functionality continued to work as before without any account locking or enforced delay.
  - Status: FAIL



** Acknowledgements**

- [Selenium](https://www.selenium.dev/)
- [Python](https://www.python.org/)
- [Jira](https://www.atlassian.com/software/jira)
