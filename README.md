# DAML WITH AUTH

The goal of this repo is to provide an example of a simple daml app with Auth0 protection
AuthT and AuthZ for Navigator, JSON API client and UI

## Launch tips
```
daml sandbox --config auth.conf
```
```
daml ledger upload-dar --host localhost --port 6865 --access-token-file m2m-access.token .daml/dist/daml-with-auth-0.0.1.dar
```
```
daml script --dar .daml/dist/daml-with-auth-0.0.1.dar --script-name Test:allocateParties --access-token-file m2m-access.token --ledger-host localhost --ledger-port 6865
```
```
daml ledger list-parties --host localhost --port 6865 --access-token-file m2m-access.token 
```
```
token : {"admin": true, "actAs": ["Alice::1220dcfdf8c383f01ecc8a1d0147ec5ef58cfa1939736da62bbecc774e836b50a8bc", "Bob::1220dcfdf8c383f01ecc8a1d0147ec5ef58cfa1939736da62bbecc774e836b50a8bc"]}
```