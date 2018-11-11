# Kuehl

An IoT grocery shopping list for your fridge.

## Installation

1. Install Arduino libraries:
   - `Adafruit Neopixel`: search for it in the Arduino IDE
   - `ArduinoJson`: search for it in the Arduino IDE. Make sure to install version `5.x`.
   - `WifiManager`: on its [Github page](https://github.com/tzapu/WiFiManager/tree/development), click on `Clone or Download` and then on `Download ZIP`. Add the ZIP in the Arduino IDE as a library.
2. In the serial monitor, make sure to choose `115200 baud`.
3. Flash the sketch

## Wifi and Todoist Configuration

1. Take note of the information in the serial monitor:

```
***************************************************
* No Wifi configuration or not possible to connect.
* Entered config mode. Connect to me using:
*
* Wifi SSID: Kuehl01
* Wifi Password: 123456ABCDEF
* Web IP address: 192.168.4.1
***************************************************
```

2. Connect to the given Wifi
3. Visit the given IP address in your web browser
4. Click on `Configure Wifi`
5. Enter the SSID and the password of the Wifi you want to connect to
6. Enter your [Todoist](https://todoist.com) token (can be found on the [integration page](https://todoist.com/prefs/integrations))
7. Enter your Todoist project ID which is used to add groceries to. To get the project ID, open the project on [Todoist](https://todoist.com) and copy it from the URL, e.g. `https://todoist.com/app#project%2F1234567890%2Ffull`. Do not copy any of the `%2F`. In this example, the project ID would be `1234567890`.
8. Click `Save`.

If all information has been entered correctly, the access point is being shut down and the device connects to your wifi. It then reports its IP address in the serial monitor.

## Usage

Click any key on the keypad to add a task to the configured Todoist project.

Use the `*` key to reset Wifi settings and restart the device. It then acts as an access point and needs to be configured again.
