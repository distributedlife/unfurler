# unfurler
Support functions for unfurling an array

# Usage
Takes an array of functions and returns a function that calls all the functions within it.

```javascript
var a = function() { console.log("a"); };
var b = function() { console.log("b"); };
var unfurled = require('unfurler').array([a, b]);
unfurled();
//a
//b
```

If given a single function it just returns that function.

```javascript
var a = function() { console.log("a"); };
var unfurled = require('unfurler').array(a);
unfurled();
//a
```

If asked for a guarantee it will return an empty function rather than return undefined.

```javascript
var unfurled = require('unfurler').arrayWithGuarentee();
unfurled(); //doesn't crap out.
```