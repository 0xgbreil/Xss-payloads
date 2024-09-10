# -Xss-payloads-
Some  lists of XSS payloads
# Stored XSS (Persistent XSS)

Stored XSS occurs when the injected script is stored on the server, typically in a database, and then displayed to users who access the affected page. This type of XSS is considered more dangerous because the malicious script is executed every time the page is loaded by any user, including administrators.

## Example:

```html
<script>alert('Stored XSS')</script>

