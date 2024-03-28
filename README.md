# cilogon_jlab


# Jefferson Lab CILOGON Policy 

## Rucio

Q. ** What is the Audience for CILOGON of Jlab**
### Rucio Auth Client
- OIDC Client ID: `cilogon:/client_id/24137530d65adc8d345dac09a2e93049`

- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- |---------|
    | WLCG  | toke_exchange, token_refresh, authorization_code | openID, profile, rucio | ? |


### Rucio Admin client
- OIDC Client ID: `cilogon:/client_id/68adabb818f03f802efe43eb806d35f5`
- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- | --------|
    | WLCG  | client_credentials | scim:read | ? |


## FTS3
- OIDC Client ID: `Need to create it`

- Policy:

    | Token Profile    | Grant Types  | Scopes| Audience |
    | -------- | ------- | -------- | --------|
    | WLCG  | offline_access| storage.read:/ storage.create:/ storage.modify:/ fts | ? |
