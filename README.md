# Home Automation with Home Assistant <img align = "right" width="30" height="30" src="./docs/HA_Icon.jpg">

**Home automation project using Home Assistant for IoT device monitoring and control**

<img align = "right" width="300" height="200" src="./docs/logo.jpg">

----

<div align="justify"> 

**Overview**

Transform your home into a smart space with this Home Assistant project. Easily monitor and control your IoT devices from a single dashboard. Enjoy automated tasks, energy efficiency, and enhanced comfort. This project provides a step-by-step guide to building your own home automation system. [learn-more](https://www.home-assistant.io/)

</div>

----

**Installation**
  
[Go here](https://www.home-assistant.io/installation/) and here install the type of installation you are comfortable with & follow each step mention properly.

</div>

----

**Steps**

1. Install Home Assistant OS: Follow the on-screen instructions after booting from the downloaded image.
2. Access Home Assistant: Open a web browser and go to the IP address. 
    `Default IP address` (http://homeassistant.local:8123/), if this doesn't work you have to find your server's IP either from below:
  - `HomeAssitant CLI` : 
    - <img width="600" height="250" src="./docs/CLI.jpg">
  - `Router's devices list` : 
    - <img width="400" height="300" src="./docs/RouterList.jpg ">

3. Configure: Set up your account, location, and time zone. [follow-this-steps](https://www.home-assistant.io/getting-started/onboarding)
4. Integrate Devices: Add your IoT devices using the Home Assistant integration page.

----

<div align="justify"> 

## Customization with EspHome: <img width="100" height="25" src="./docs/EspHome_Icon.jpg">

**Add Esphome to Home Assistant:** 

- Go to -`Settings > Add-on Store > Search for " Esphome "`
  
<img width="600" height="300" src="./docs/EspHome_addon.jpg">

- `click install and start add-on`

<img width="700" height="400" src="./docs/EspHome_addon_Start.jpg">

- `Go to Esphome menu on the left`
  
<img width="700" height="400" src="./docs/EspHome_Setup.jpg">

- `Add a new device by clicking new device`
- It will take you here : [Setup_newBoard](https://web.esphome.io/?dashboard_wizard)
- Connect the Esp-Board to the computer or laptop on which you have opened the Home Assistant dashboard for the setup.
<img width="350" height="400" src="./docs/Esp-add_device.jpg">

- click `connect` and select your device if shown in the list if not reconnect or check for suitable drivers for your board
- Follow the next steps like `wifi credentials` and upload the EspHome firmware
-  Now your device will be shown in the esphome tab & you edit the code:

----

**Here is example of controlling A Led and monitoring value of an analog sensor**

<img align = "right" width="550" height="400" src="./docs/Led_Control.gif">

```yaml

switch:
  - platform: gpio
    name : "LED"
    pin:
      number: GPIO2
      inverted: true

sensor:
  - platform: adc
    pin: VCC
    name: "power level"

```
<img align = "left" width="300" height="150" src="./docs/Led_sample.gif">

</div>