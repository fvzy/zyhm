# zyhm
<p align="center">
<a target="_blank" href="https://github.com/wffzy"><img src="https://avatars.githubusercontent.com/wffzy?s=400&u=ce99f02d685d58b2bc8b381afa7868481515dbe7&v=4" alt="" width="169" /></a>
</p>
<p align="center">
<a target="_blank" href="https://github.com/wffzy"><img title="Author" src="https://img.shields.io/badge/Author-Ditzzy-red.svg?style=for-the-badge&logo=github" /></a>
<br>
<a target="_blank" href="//npmjs.com/caliph-api"><img src="https://img.shields.io/npm/dw/zyhm?color=yellow&label=Downloads&logo=npm&style=flat"></a>
<br>
<a target="_blank" href="https://www.npmjs.com/package/zyhm?activeTab=versions"><img src="https://img.shields.io/npm/v/zyhm?color=green&label=version&logo=npm&style=social"></a>
</p>

# Note
This is a library that allows you to remotely control your web hosting server that is running cPanel for personal or bot use.</br>
Recoded and fixing outlog from : [`@ihadeed/node-whm`](https://github.com/ihadeed/node-whm)


### Instalation
<code>GITHUB</code>
```bash
npm i git+github.com/wffzy/zyhm
```

<code>NPM</code>
```bash
npm i zyhm
```

### Usage JavaScript

```javascript
var ZYHM = require('zyhm');
var ZYHMClient = new ZYHM.Client({
    serverUrl: 'https://myserver.com:2087',
    remoteAccessKey: 'remoteAccessKeyHere',
    username: 'resellerOrRootUser'
});

ZYHMClient.createAccount({
    username: 'myuser',
    password: 'mySecurePassword!',
    plan: 'Pro',
    domain: 'clientdomain.com'
}).then(
    function(success){ 
        console.log(success);
        // do something with data
    },
    function(error) {
        console.error(error);
        // do something with data
    }
);

```
### Usage Typescript
```typescript
import { Client, ZYHMOptions } from 'zyhm';

const ZYHMClientOptions: ZYHMOptions = {
   serverUrl: 'https://myserver.com:2087',
   remoteAccessKey: 'remoteAccessKeyHere',
   username: 'resellerOrRootUser'
};

const client: Client = new Client(ZYHMClientOptions);

client.createAccount({
           username: 'myuser',
           password: 'mySecurePassword!',
           plan: 'Pro',
           domain: 'clientdomain.com'
       }).then(
           success => { 
               console.log(success);
               // do something with data
           },
           error => {
               console.error(error);
               // do something with data
           }
       );
```
## Methods Calling Function

#### `createAccount(options: CreateAccountOptions): Promise<any>`
#### `terminateAccount(user: string): Promise<any>`
#### `listAccounts(): Promise<AccountData[]>`
#### `listIPAddresses(): Promise<any>`


## Interfaces _`TypeScript`_

#### `WHMOoptions`
#### `CreateAccountOptions`
#### `AccountData`

