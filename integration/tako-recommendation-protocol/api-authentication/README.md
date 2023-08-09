# API: Authentication

## Overview

Part of the APIs on Tako must use authentication.

We use JWT as the authentication layer. After logging in, you will receive two tokens: access token and refresh token.

Below is the login process:

1. Use the EVM wallet to sign a message and get the sign string.
2. Send the sign string to GetToken API
3. API will do the login works, then return access token and refresh token for you

The access token is the only credential to access APIs, so you must save it securely. Its validity period is 3600 seconds. You can use the refresh token to refresh the access token. Its validity period is 86400 seconds.

## APIs

{% content-ref url="gettoken.md" %}
[gettoken.md](gettoken.md)
{% endcontent-ref %}

{% content-ref url="refreshtoken.md" %}
[refreshtoken.md](refreshtoken.md)
{% endcontent-ref %}
