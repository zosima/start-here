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

- Trigger
  * Trigger Fired

### What we've got

1. Philips Hue lights
1. Belkin Wemo Sensor
1. Belkin Wemo Power Switch
1. Harmony Remote
1. BLE Proximity Detection?

### Moving Parts

* An Android app
  - Polls various devices that are on the local network (lights, sensors,
    switches)
  - Recieves various push notifications that tell us to do stuff on the local
    network

* A Rails Website
  - Handles push notification tokens and sends pushes
  - Allows the Android app to add items to the event table via API
  - UI for starting scenes yourself (mobile)
  - UI for saving scenes (desktop)
  - UI for auto-starting scenes based on triggers (desktop)

### To complete scenario one, we need

1. An Android app logs into the website, registers for push notifications
1. On the app, we have a page to set up the Philips Hue and do the UDP dance
1. The app registers the new Devices that it finds with the website API
1. On the website, we capture a state then create a Scene
1. On the mobile website, the user asks to move into a Scene, we ping the
   Mobile site which pushes the state data to the Android app.
1. The Android app applies the state
