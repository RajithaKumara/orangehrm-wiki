## REST API
## How to authenticate 
* it's a Bearer token authentication
* before you can use the API you need to create an OAuth client from the OrangeHRM web UI in `Admin > Configuration > Register OAuth Client` by giving it secure id and secret/password.
* In order to authenticate, a POST request is fired to `{your-host}/index.php/oauth/issueToken` (in my case http://127.0.0.1/orangehrm-4.0/symfony/web/index.php/oauth/issueToken)
* the request takes parameters client_id, client_secret, grant_type , where

client_id = [the oauth ID you've created];
client_secret = [the oauth secret you've created];
grant_type = 'client_credentials'

* the response looks like `{"access_token":"ecdc9f1c565ce501f25c7b9a1b17d4d254d35f50","expires_in":3600,"token_type":"bearer","scope":null}`
* now you can call the API with an Authorisation header: {[token_type] [access_token]} (e.g. `Authorisation: "Bearer ecdc9f1c565ce501f25c7b9a1b17d4d254d35f50"` at `http://{your-host}/api/v1/*`

## Documentation 
Rest API docs are avaliable in https://orangehrm.github.io/orangehrm-api-doc/