# Jefferson Lab CILOGON Policy 

## Rucio

Q. ** What is the Audience for CILOGON of Jlab**
### Rucio Auth Client
- OIDC Client ID: `cilogon:/client_id/24137530d65adc8d345dac09a2e93049`
- issuer: `https://cilogon.org/jlab`
- VO: `prod:jlab/jlab` 
- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- |---------|
    | WLCG  | token_exchange, token_refresh, authorization_code | `openID`, `profile` | ? |


    - Access token lifetime : 1 hour 
    - Allow token for COU : `CO:COU:eic:members:active`

### Rucio Admin client
- OIDC Client ID: `cilogon:/client_id/68adabb818f03f802efe43eb806d35f5`
- issuer: `https://cilogon.org/jlab`
- VO: `prod:jlab/jlab` 
- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- | --------|
    | WLCG  | client_credentials | `scim:read` | ? |


    - Access token lifetime : 1 hour 

## FTS3
- OIDC Client ID: `cilogon:/client_id/7539b687ee887157195a9dc1aefb3fc2`
- issuer: `https://cilogon.org/jlab`
- VO: `prod:jlab/jlab` 
- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- | --------|
    | WLCG  | token_exchange, token_refresh | `storage.read:/` ,  `storage.create:/` , `storage.modify:/` ,  `fts`, `openID`, `profile`, `email`, `offline_access`| ? |


    - Access token lifetime : 1 hour 
