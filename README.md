# mwl-loudness

A node.js library to control the systems output volume
fork from https://github.com/LinusU/node-loudness.
added hazardous package for electron, fixed that the electron app can't find the correct path
which in the "app.asar.unpacked" folder.

## Usage

The library currently has support for four simple async functions. The volume is specified as an integer between 0 and 100 (inc.).

```javascript
const loudness = require('loudness')

loudness.setVolume(45).then(() => {
  // do something..
})

loudness.getVolume().then((val) => {
  // val is current system volume.
  // do something..
})

loudness.setMuted(false).then(() => undefined)

loudness.getMuted().then((muted) => {
  // muted
})
```

## OS Support

Currently Mac OS X,  Linux (ALSA) and Windows NT is supported
