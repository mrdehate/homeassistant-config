# Mark D's Home Assistant Configuration
This is my Home Assistant (hassio) configuration!

## Hardware
* Raspberry Pi 3
* Aeotec [Z-Stick Gen5 (ZW090)](https://amzn.to/2GjobGA)
* Dresden Elektronik [Conbee Zigbee Gateway](https://amzn.to/2TuA9Rw)

## Connected Devices

I've really tried to stick with Z-Wave products for simplicity, though there are a few outliers for various reasons.

### Z-Wave
#### Switches & Dimmers (In-Wall)
* Leviton, either the Decora [Smart Switches (DZ15S-1BZ)](https://amzn.to/2D1HXDa) or [Dimmers (DZ6HD-1BZ)](https://amzn.to/2SoMIjY)
  * These are really great, and respond instantaneously! My preferred option.
* [HomeSeer HS-WS200+](https://amzn.to/2WD5i7d)
  * I have these only where I need to use the scene functionality, and where I can deal with the .5 second-ish delay they come with (like outdoor lights).

#### Outlets (In-Wall)
* [Jasco outlets, either GE or Honeywell brand](https://amzn.to/2WFqysP)

#### Outlets (Plug-In)
* [GE Outdoor (14284)](https://amzn.to/2Tvk0Lu)
* [Leviton (DZPA1-2BW)](https://amzn.to/2WzqAmh)
* Inovelli Dual Outlet (NZW37)

#### Sensors
* [Monoprice Z-Wave Plus Door & Window Sensor (24259)](https://amzn.to/2ML5mx6)
* [Zooz 4-in-1 Sensor (luminance, motion, humidity, temperature) (ZSE40, version 2)](https://amzn.to/2Glossr)
* [Ecolink Door and Window Sensor (DWZWAVE2.5-ECO)](https://amzn.to/2TppjMh) (see Bed Presence Detection section below for why I'm using this one)

### Zigbee
I tried really hard to avoid having any Zigbee devices (well, non-Hue anyway), but the price of these Xiaomi sensors suckered me in.

* Xiaomi Aqara Temperature Sensor (WSDCGQ11LM)

### Connected Bulbs
All my connected bulbs go through the Philips Hue hub
* Phillips Hue Bulbs
  * Dimmable/White Ambiance/Full Color in BR30 & A19
* GLEDOPTO ZLL Light Controller (x2)
  * Controls some standard RGB LED roll lights, SMD 5050

### Media Players
* Chromecast Audio
* Also connected are Plex, Roku, and Spotify, though not particularly useful to me

### Presence Detection
* OwnTracks, for both iOS and Android

#### Bed Presence
I have an Ecolink Door and Window sensor connected to a [Ideal Security SOLO pressure mat](https://amzn.to/2TomSd0) - the Ecolink has easily accessible terminals for connecting an external sensor. This is used for detecting if anyone is in bed. The pressure mat is rated to trigger at 1lb of force per square inch.

I have a Tuft and Needle king-size memory foam mattress, with a wood slat base. I wasn't able to get the pressure mat to work reliably underneath the mattress, which was my original goal. The mat is pretty crinkly, so it's not great to go right under the bed sheet, but I have found success putting it underneath my pillow. It probably helps that I have the somewhat thick electric mattress heating pad to slide it under too.

### Miscellaneous/Wifi
* Google Home/Home Hub/Home Mini
* Belkin Wemo wifi switches
* [Gogogate2](https://amzn.to/2MM4gRN) garage door opener
* Automatic Pro car adapter
* OwnTracks App for iOS/Android

### Non-Smart Devices Being Controlled
* [QuietCool Whole House Fan](https://quietcoolsystems.com/) (plugged into a GE in-wall smart outlet in the attic)
* [Biddeford Electric Mattress Heating Pad](https://amzn.to/2TtzDmu) (5902-908221-100)
  * Note on this, most electric heating pads are digital, which means they don't turn on automatically when power is applied. This one in particular still has a physical switch and dial, which is great. 
* Lepai Class-D Amplifiers (LP-2020A & similar), and a hodgepodge of mostly low-end PC speakers/subs
* Disco Ball


## Notable Automations

### Lights
* Turn on/off overhead garage lights with garage door
  * The lights in my garage door opener are really flaky; this is a bit overkill, but handy anyway.
* Presence-based away mode (turn off lights when everyone leaves home)
* Turn on/off sets of lights with multi-tap of HomeSeer switches
  * All outdoor lights
  * All kitchen lights
  * All basement lights (from top of basement stairs)
* Turn on entry lights when garage door opens
  * Someday would like to make this presence-based, but I'm still not real confident in my presence solution.

### Other Stuff
* Turn on amplifiers when sound is playing to the connected Chromecast Audio
  * I have a few sets of powered speakers throughout the house hooked to Chromecast Audios, and this ensures the amps aren't sucking power all day for no reason.
  * Unfortunately Google Cast groups are super flaky in my experience, so this doesn't work 100% of the time - some groups are better than others.
* Turn on heated mattress pad before bed, based on the room temperature.
* Safety switch to turn off whole house fan if insufficient ventilation.
* Automatically close garage door every night in case it's left open.