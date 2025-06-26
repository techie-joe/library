# HTML5 and Internet Explorer

## IE needs 512+ bytes
IE5+ (including IE9) will replace your custom HTTP error response (e.g. 404, 500)
with its own "friendly" message — unless the response body is longer than ~512 bytes.

###💡 Why it happens:
IE tries to be "helpful" by showing a default error page if your response body is too short.

### 🧠 IE's “Friendly Error Pages” Trigger On:
512-byte quirk in IE only applies to specific HTTP error status codes — not normal pages.

- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found
- 405 Method Not Allowed
- 406 Not Acceptable
- 408 Request Timeout
- 409 Conflict
- 410 Gone
- 500 Internal Server Error
- 501 Not Implemented
- 505 HTTP Version Not Supported

If the response body is <512 bytes, IE replaces it with its own “friendly” default page.

### ✅ Normal pages (200 OK)?
✅ Not affected.
IE doesn’t mess with them — your content is shown as-is, no byte minimum needed.

### 🔒 Dev Tip:
If you're serving error pages through Express, always make sure your custom error templates are >512 bytes — just to be safe — if you're still supporting IE (which, again, you probably shouldn't 😅).

> Read [Friendly HTTP Error Pages](https://docs.microsoft.com/archive/blogs/ieinternals/friendly-http-error-pages)