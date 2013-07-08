# reflecta_hart1 #

reflecta_hart1 binds the function setFrameRate to the hart1 interface.  This is the Arduino library that enables heartbeats with data coming from the Arduino to be frame rate controlled by the receiver.

> _Stability: Medium_

## Calling reflecta_hart1 from NodeJS

Simply load reflecta using

```
npm install reflecta
```

```javascript
var reflecta = require('reflecta');

reflecta.detect(function(error, boards, ports) {

    board = boards[0];

    if (board.hart1) {
        board.hart1.setFrameRate(20);
    }
});
```

Reflecta will use npm to install and load this library automatically if the Arduino exposes the 'hart1' interface.

A [simple but complete example](https://github.com/JayBeavers/node-reflecta/blob/master/samples/simple.js) can be found in the node-reflecta project.

## Release History

- 0.1.0: Initial release