# Mark D's Home Assistant Configuration
This is my Home Assistant (hassio) configuration!

## Hardware
* Raspberry Pi 3
* Aeotec Z-Stick Gen5 (ZW090)

## Connected Devices

### Z-Wave
* Switches (In-Wall)
 * Mostly Leviton, either the Decora Smart Switches (DZ15S-1BZ) or Dimmers (DZ6HD-1BZ)
 * Some HomeSeer - HS-WS200+
* Outlets (In-Wall)
 * Jasco - GE/Honeywell
* Outlets (Plug-In)
 * GE Outdoor (14284)
 * Leviton (DZPA1-2BW)
 * Inovelli Dual Outlet (NZW37)
* Sensors
 * Monoprice Z-Wave Plus Door & Window Sensor (24259)
 * Zooz 4-in-1 Sensor (luminance, motion, humidity, temperature) (ZSE40, version 2)

### Connected Bulbs
All my connected bulbs go through the Philips Hue hub
* Phillips Hue Bulbs
 * Dimmable/White Ambiance/Full Color in BR30 & A19
* GLEDOPTO ZLL Light Controller
 * Controls some standard RGB LED roll lights, SMD 5050

### Media Players
* Chromecast Audio
* Also connected are Plex, Roku, and Spotify, though not particularly useful

### Miscellaneous/Wifi
* Google Home/Home Hub/Home Mini
* Belkin Wemo wifi switches
* Gogogate2 garage door opener
* Automatic Pro car adapter
* OwnTracks App for iOS/Android

### Non-Smart Devices Being Controlled
* QuietCool Whole House Fan
* Biddeford Electric Mattress Heating Pad (5902-908221-100)
* Lepy Class-D Amplifiers (LP-2020A), and a hodgepodge of mostly low-end PC speakers/subs
* Disco Ball


## Automations

* Turn on/off overhead garage lights with garage door
* Presence-based away mode (turn off lights when everyone leaves home)
* Turn on/off sets of lights with multi-tap of HomeSeer switches
 * All outdoor lights
 * All kitchen lights
 * All basement lights (from top of basement stairs)
* Turn on amplifiers when sound is playing to the connected Chromecast Audio