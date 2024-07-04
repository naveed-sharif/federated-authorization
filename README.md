# federated-authorization


# OAuth2 Token Retrieval using cURL

This document provides instructions on how to retrieve an OAuth2 token from a local server using the `curl` command-line tool.

## Prerequisites

- Ensure `curl` is installed on your local machine.

## Steps to Retrieve Token

1. **Requesting Token**

   Use the following `curl` command to request an OAuth2 token:

   ```bash
   curl --location 'http://localhost:9090/oauth2/token' \
   --header 'Content-Type: application/x-www-form-urlencoded' \
   --header 'Authorization: Basic Y2xpZW50MS1pZDpjbGllbnQxLXNlY3JldA==' \
   --header 'Cookie: JSESSIONID=4DC4896AC338D1D15EC0FE8D2B500156' \
   --data-urlencode 'grant_type=client_credentials'
   ```

   - Replace `http://localhost:9090/oauth2/token` with your token endpoint URL.
   - Modify the `Authorization` header (`Basic Y2xpZW50MS1pZDpjbGllbnQxLXNlY3JldA==`) with your client credentials encoded in Base64.
   - Adjust the `Cookie` header (`JSESSIONID=4DC4896AC338D1D15EC0FE8D2B500156`) as per your session ID.

2. **Response**

   Upon successful authentication, the server will respond with an OAuth2 token.

---

Feel free to customize this README with additional details specific to your application or environment.