# Encrypt Module

Encrypt module for gracenode framework.

This is designed to function within gracenode framework.

## How to include it in my project

To add this package as your gracenode module, add the following to your package.json:

```
"dependencies": {
        "gracenode": "",
        "gracenode-encrypt": ""
}
```

To use this module in your application, add the following to your gracenode bootstrap code:

```
var gracenode = require('gracenode');
// this tells gracenode to load the module
gracenode.use('gracenode-encrypt');
```

To access the module:

```
// the prefix gracenode- will be removed automatically
gracenode.encrypt
```

Access
<pre>
gracenode.encrypt
</pre>

Configurations
N/A

###API: createHash

<pre>
void createHash(String sourceStr, Int cost, Function callback)
</pre>

Creates a hash with salt from **sourceStr**

This function uses <a href="https://github.com/ncb000gt/node.bcrypt.js/">bcrypt</a> module and it is based on blowfish encryption.

Bigger the cost the slower this function will become.

###API: validateHash

<pre>
void validateHash(String str, String hash, Function callback)
</pre>

Validates a hash and **str**

###API: uuid

<pre>
String uuid(Int version, Object options, Buffer buffer, Array offset)
</pre>

Creates a uuid. This module uses <a href="https://github.com/broofa/node-uuid">node-uuid</a> module.

Possible values for **version** are *1* or *4*

Version 1 is timestamp-base and version 4 is random-base

