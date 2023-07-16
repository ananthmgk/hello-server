# hello-server

## Run node-server
```
PS> cd .\node-server\
PS> node .\app.js
Hello Server running at http://127.0.0.1:4000/

```

## Run express-server
```
PS> node .\app.js
node:internal/modules/cjs/loader:1078
  throw err;
  ^

Error: Cannot find module 'express'
Require stack:
    at Module._resolveFilename (node:internal/modules/cjs/loader:1075:15)
    at Module._load (node:internal/modules/cjs/loader:920:27)
    at Module.require (node:internal/modules/cjs/loader:1141:19)
    at require (node:internal/modules/cjs/helpers:110:18)
    at Object.<anonymous> \app.js:1:17)
    at Module._compile (node:internal/modules/cjs/loader:1254:14)
    at Module._extensions..js (node:internal/modules/cjs/loader:1308:10)
    at Module.load (node:internal/modules/cjs/loader:1117:32)
    at Module._load (node:internal/modules/cjs/loader:958:12)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:81:12) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    'C:\\Users\\usha\\Projects\\tmp\\hello-server\\express-server\\app.js'
  ]
}

Node.js v18.16.0
PS> npm ci

added 58 packages, and audited 59 packages in 9s

8 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
PS> node .\app.js
Example app listening on port 3000
```


## Using ngrok to tunnel the local application to internet

1. Signup of ngrok account
2. Install the ngrok (download the binary and put in PATH)
3. configure the auth token
```
ngrok config add-authtoken <my-token>
```
4. Tunnel the local port
```
ngrok http 3000
```