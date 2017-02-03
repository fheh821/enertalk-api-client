# EnerTalk API Client
The EnerTalk API Wrapper for convenience

## Getting Started

#### Install Package
```sh
> npm install enertalk-api-client
```

#### Import Package
```js
const EnerTalkAPI = require('enertalk-api-client');

or

import EnerTalkAPI from 'enertalk-api-client';
```

#### Make an instance
```js
const api = new EnerTalkAPI(authConfig, options);
```

#### Use methods with promise
```js
api.getUser()
  .then(response => console.log(response.data))
  .catch(error => console.log(error.response.data));
```


## Auth Config
```js
const api = new EnerTalkAPI({
  accessToken: 'yourAccessToken', // required
  refreshToken: 'yourRefreshToken', // optional
  clientId: 'yourClientId', // optional
  clientSecret: 'yourClientSecret', // optional
  domain: 'yourCustomAuthServerDomain', // optional, override
});
```
> The prameters `refreshToken`, `clientId`, `clientSecret`, `domain` are
> used to issue new access token.


## Options
This options follow [axios request config](https://github.com/mzabriskie/axios#request-config)
For example,
```js
const api = new EnerTalkAPI(authConfig, {
  baseURL: 'yourCustomResourceServerDomain',
  timeout: 10000,
});
```


## Supported API Methods

`getUser:` Get user profile  
`listSites:` List sites  
`listDevicesOfSite:siteIds` List devices of multiple sites  
`getBills:siteId` Get bill information  

...

These will continue to be added.