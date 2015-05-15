# webpack-pusher

This is to demonstrate the issues we're seeing with pusher when used in combination with webpack.

## Reproduce
First run `npm install` to install the dependencies. Afterwards run `webpack`

## The issues

We get the following output in the console:

```
WARNING in ./~/pusher/~/request/lib/optional.js
Critical dependencies:
11:13-32 the request of a dependency is an expression
 @ ./~/pusher/~/request/lib/optional.js 11:13-32

ERROR in ./~/pusher/~/request/request.js
Module not found: Error: Cannot resolve module 'net' in /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request
 @ ./~/pusher/~/request/request.js 36:10-24

ERROR in ./~/pusher/~/request/~/tunnel-agent/index.js
Module not found: Error: Cannot resolve module 'net' in /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request/node_modules/tunnel-agent
 @ ./~/pusher/~/request/~/tunnel-agent/index.js 3:10-24

ERROR in ./~/pusher/~/request/~/tunnel-agent/index.js
Module not found: Error: Cannot resolve module 'tls' in /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request/node_modules/tunnel-agent
 @ ./~/pusher/~/request/~/tunnel-agent/index.js 4:10-24

ERROR in ./~/pusher/~/request/~/forever-agent/index.js
Module not found: Error: Cannot resolve module 'net' in /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request/node_modules/forever-agent
 @ ./~/pusher/~/request/~/forever-agent/index.js 6:10-24

ERROR in ./~/pusher/~/request/~/forever-agent/index.js
Module not found: Error: Cannot resolve module 'tls' in /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request/node_modules/forever-agent
 @ ./~/pusher/~/request/~/forever-agent/index.js 7:10-24

ERROR in ./~/pusher/~/request/~/mime-types/lib/mime.json
Module parse failed: /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request/node_modules/mime-types/lib/mime.json Line 2: Unexpected token :
You may need an appropriate loader to handle this file type.
| {
|   "application/1d-interleaved-parityfec": [],
|   "application/3gpp-ims+xml": [],
|   "application/activemessage": [],
 @ ./~/pusher/~/request/~/mime-types/lib/index.js 11:8-30

ERROR in ./~/pusher/~/request/~/mime-types/lib/node.json
Module parse failed: /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request/node_modules/mime-types/lib/node.json Line 2: Unexpected token :
You may need an appropriate loader to handle this file type.
| {
|   "text/vtt": [
|     "vtt"
|   ],
 @ ./~/pusher/~/request/~/mime-types/lib/index.js 12:8-30

ERROR in ./~/pusher/~/request/~/mime-types/lib/custom.json
Module parse failed: /Users/danielapt/Desktop/webpack-pusher/node_modules/pusher/node_modules/request/node_modules/mime-types/lib/custom.json Line 2: Unexpected token :
You may need an appropriate loader to handle this file type.
| {
|   "text/jade": [
|     "jade"
|   ],
 @ ./~/pusher/~/request/~/mime-types/lib/index.js 13:10-34

```
