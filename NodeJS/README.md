## Upgrade npm

`sudo npm install npm -g`

## Concat two arrays

```javascript
[1,2,3].concat([4,5,6])
```

## Define module and usage

```javascript
// Define module

"use strict";
const
    util = require('util'),
    net = require('net'),
    // server constructor
    NetWatcherServer = function(handler) {
        return net.createServer(handler);
    };

// expose module methods
exports.NetWatcherServer = NetWatcherServer;
exports.createServer = function(handler){
    let server = new NetWatcherServer(handler);
    server.listen(5432, function() {
        console.log('Listening for subscribers...');
    });
    return server;
};

// Module usage:
"use strict";
const netWatcher = require('./net-watcher-server.js');
netWatcher.createServer(function(connection) {
  console.log("using the module!");
});

```
## brew Could not symlink, /usr/local/bin is not writable

When installing various packages for `nodejs` you might come up upon this, issue this:

```bash
sudo chown -R `whoami`:admin /usr/local/bin
```
