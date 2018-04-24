<a href="https://codeclimate.com/github/Evanion/config-extended/maintainability"><img src="https://api.codeclimate.com/v1/badges/bb7eafcb9c2fdb96697a/maintainability" /></a>
<a href="https://codeclimate.com/github/Evanion/config-extended/test_coverage"><img src="https://api.codeclimate.com/v1/badges/bb7eafcb9c2fdb96697a/test_coverage" /></a>
[![CircleCI](https://circleci.com/gh/Evanion/config-extended.svg?style=svg)](https://circleci.com/gh/Evanion/config-extended)

# config-extended
An easy to use package to handle configuration in your Node.js application.
This package extends the standard [config](https://www.npmjs.com/package/config) package to automatically resolve
environment variables.

## Example
```
# DB_INFO=mongo://localhost:27017/example npm start
```
config/default.json
```
{
  "database": "DB_INFO"
}
```

index.js
```
import Config from '@evanion/config-extended';

const dbHost = Config.get('database'); // > mongo://localhost:27017/example
```
