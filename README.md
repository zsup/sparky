Sparky
=============================
Sparky is a simple node.js library for communicating with a Spark core.

Installation
-----------------------------
```
npm install sparky
```

Usage
-----------------------------
Turn the built-in LED on.

```
var Sparky = require('sparky').Sparky

var sparky = new Sparky({
	deviceId: 'your device id',
	token: 'your access token',
})
sparky.digitalWrite('D7', 'HIGH');
```

Blinking the built-in LED.

```
var Sparky = require('sparky').Sparky

var sparky = new Sparky(config);
var val = 0;
(function toggle() {
	val = 1 - val;
	sparky.digitalWrite('D7', val);
	setTimeout(toggle, 1000);
})();
```

Run a custom command from your SparkCore firmware.
```
var Sparky = require('sparky').Sparky

var sparky = new Sparky({
	deviceId: 'your device id',
	token: 'your access token',
})
sparky.run('MyCustomFunction', 'what,ever,you,want', callback);
```

