# Jefferson Lab CILOGON Policy 

## Rucio

Q. ** What is the Audience for CILOGON of Jlab**
### Rucio Auth Client
- OIDC Client ID: `cilogon:/client_id/24137530d65adc8d345dac09a2e93049`

- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- |---------|
    | WLCG  | token_exchange, token_refresh, authorization_code | `fts` `wlcg.groups` `offline_access` | ? |


    - Access token lifetime : 1 hour 
    - This should have `offline_access`.
    - ID token should provide at minimum `openid` and `email`
    - Allow token for COU : `CO:COU:eic:members:active`

### Rucio Admin client
- OIDC Client ID: `cilogon:/client_id/68adabb818f03f802efe43eb806d35f5`
- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- | --------|
    | WLCG  | client_credentials | `scim:read` `fts` `offline_access` `wlcg.groups` | ? |


    - Access token lifetime : 1 hour 
    - This should have offline access.
    - **The grant_type `client_credentials` is not available.**
    - **So lets try `eratz_client` for now and we will revisit.**

## FTS3
- OIDC Client ID: `cilogon:/client_id/7539b687ee887157195a9dc1aefb3fc2`

- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- | --------|
    | WLCG  | token_exchange, token_refresh | `storage.read:/eic` ,  `storage.create:/eic` , `storage.modify:/eic` ,  `fts`,  `offline_access`| ? |

    - Access token lifetime : 1 hour 
    - This should have `offline_access`.