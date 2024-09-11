# -Xss-payloads-
Some  lists of XSS payloads
# Understanding Cross-Site Scripting (XSS)

## Introduction

Cross-Site Scripting (XSS) is a security vulnerability that allows attackers to inject malicious scripts into web pages viewed by other users. XSS vulnerabilities occur when web applications fail to properly sanitize user inputs, allowing attackers to execute scripts in the context of the victim's browser. These scripts can steal sensitive information like cookies, session tokens, or redirect users to malicious websites.

XSS is one of the most common security vulnerabilities in web applications, and it is often listed in the OWASP Top 10. Understanding XSS is critical for securing web applications and protecting users.

## Types of XSS

XSS vulnerabilities generally fall into three main categories:

### 1. **Stored XSS (Persistent XSS)**

Stored XSS occurs when the injected script is stored on the server, typically in a database, and then displayed to users who access the affected page. This type of XSS is considered more dangerous because the malicious script is executed every time the page is loaded by any user, including administrators.

#### Example:

```html
<script>alert('Stored XSS')</script> 
```
مم

### 2. **Reflected XSS**




Reflected XSS occurs when the malicious script is included in a URL or form input and reflected back to the user by the server. It is executed immediately when the user interacts with the crafted link. Unlike stored XSS, the payload is not stored on the server.

## Example:

```html
https://example.com/search?q=<script>alert('Reflected XSS')</script>
```

### 3. **DOM-based XSS**



DOM-based XSS occurs on the client side, where the vulnerability exists in the web page's JavaScript code. The attack is executed when a script on the page processes input data from the URL or another DOM element without proper validation or sanitization.

## Example:

```javascript
var userInput = location.hash;
document.write(userInput);

