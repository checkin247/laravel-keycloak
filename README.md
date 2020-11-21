# Protect your laravel backend with a keycloak SSO server

This is a demonstration of how to validate a signed access token. 
This could potentially be done with other authentication provider, keycloak is open source easy to use.
For a full [step by step tutorial](https://tliebrand.com/18-sicherheit/27-authenticate-keycloak-access-token-in-laravel), visit my website.

## Credits
Keycloak guard for laravel:
[robsontenorio](https://github.com/robsontenorio/laravel-keycloak-guard/commits?author=robsontenorio)

## How does it work
This are the essential steps:

User authenticates her/him on the keycloak server and retrieves an access token. This step is not covered, but the steps involved are well covered on the keycloak documentation. Also refer to ["how to authorize a nuxt app with keycloak"](https://github.com/checkin247/nuxt-login-with-keycloak).

Because the access token is signed by the keycloak server, we can use the public key to verify its signature.

This verification is done by the laravel keycloak guard by [robsontenorio](https://github.com/robsontenorio/laravel-keycloak-guard/commits?author=robsontenorio)


