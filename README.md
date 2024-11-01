# oauth2-proxy-keycloak

I created a simple demo setup using OAuth2 Proxy with Keycloak for authentication. The setup allows users to log in through Keycloak, and OAuth2 Proxy secures access to an application by validating the tokens. This configuration provides a straightforward example of integrating Keycloak as an identity provider for OAuth2 Proxy.

## Setup

- Add `127.0.0.1   keycloak` to your `/etc/hosts`. this is necessary for the keycloak redirection
- Run `docker-compose up keycloak`
- Login to keycloak at `http://keycloak:8080` 
- Setup keycloak (create Realm,CLIENT_SECRET,Valid redirect URIs), and rewite OAUTH2_PROXY_CLIENT_SECRET value
- Run `docker-compose up web oauth2-proxy`
- Now try to login with your new user via http://localhost:3000


