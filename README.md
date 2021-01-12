# VAULT Tutorial

### Start a dev server
  - ``` vault server -dev ```

### Start a vault client session

  - Connect to vault server
    - ``` export VAULT_ADDR='http://127.0.0.1:8200' ``` 
    - ``` set VAULT_ADDR=http://127.0.0.1:8200 ```

  - Save Key and Token
    - Unseal Key: VLAmNXfWlwCobgJyY70MgVS3X0WtRL4+DiLanj5qcIc=
    - Root Token: s.7jzhwqKfPN3oO2ERyTiXoQaa

  - Setup Token
    - ``` export VAULT_TOKEN="s.7jzhwqKfPN3oO2ERyTiXoQaa" ``` 
    - ``` set VAULT_TOKEN=s.7jzhwqKfPN3oO2ERyTiXoQaa ``` 

  - Validate vault server
    - ``` vault status ```

### Put keys

  - ``` vault kv put secret/hello username=yul pw=123456 ```

### Get keys back

  - ``` vault kv get secret/hello ``` 
  - ``` vault kv get -format=json secret/hello ``` 
  - ``` vault kv get -format=json secret/hello | jq > secret.hello.json ``` 
