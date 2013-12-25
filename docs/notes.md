### Scenarios

* When we enter the house and we're in the 'Off' scene, move to the 'Reading'
  scene
* When nobody is in the house, move to the 'Off' scene
* When someone enters the bedroom, turn on the bedroom lights
* When nobody is in the living room, disable the living room lights
* When I want to watch a movie, dim the lights and turn on the TV

### Modeling

- Scene
  * List of devices affected
  * Saved state for each device

- Device
  * Get State
  * Set Saved State

### What we've got

1. Philips Hue lights
1. Belkin Wemo Sensor
1. Belkin Wemo Power Switch
1. Harmony Remote
1. BLE Proximity Detection?
