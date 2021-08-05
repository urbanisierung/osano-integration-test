# OsanoIntegrationTest

Test Osano Script Integration

The script is embedded [here](./src/index.html).

## Start locally

```bash
npm i
npm run start
```

## Tests

- Working: [http://localhost:4200/](http://localhost:4200/test/123) and [http://localhost:4200/test](http://localhost:4200/test)
  - No routing parameters
- Failing: [http://localhost:4200/test/123](http://localhost:4200/test/123)
  - App does not start
  - See browser console for errors
  - After removing Osano Script everything works as expected

Errors:

```bash
GET http://localhost:4200/test/runtime.js net::ERR_ABORTED 404 (Not Found)
GET http://localhost:4200/test/polyfills.js net::ERR_ABORTED 404 (Not Found)
GET http://localhost:4200/test/vendor.js net::ERR_ABORTED 404 (Not Found)
GET http://localhost:4200/test/main.js net::ERR_ABORTED 404 (Not Found)
```

Other (not blocking) errors:

```bash
cmp.osano.com/:18 Uncaught TypeError: data.split is not a function
    at cmp.osano.com/:18
```
