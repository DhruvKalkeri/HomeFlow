# HomeFlow — Engineering Project Portfolio

A responsive engineering case study for the HomeFlow ESP32 smart-home prototype.

## Project media

### Actual HomeFlow evidence
- `assets/images/homeflow-prototype.webp` — user-supplied photo of the branded HomeFlow prototype enclosure.
- `assets/images/homeflow-dashboard.webp` — user-supplied HomeFlow browser dashboard screenshot.
- YouTube demonstration: https://youtu.be/eD1jUGDrwWQ

### External reference media (not photographs of this build)
- ESP32 development-board photograph: Ubahnverleih, Wikimedia Commons, CC0 1.0. [File page](https://commons.wikimedia.org/wiki/File:ESP32_Espressif_ESP-WROOM-32_Dev_Board.jpg)
- Single-channel relay-module photograph: Suyash Dwivedi, Wikimedia Commons, CC BY-SA 4.0. [File page and license](https://commons.wikimedia.org/wiki/File:SRD-05VDC-SL-C_5V_one-channel_relay_module.jpg)
- Conceptual ESP32-to-relay wiring diagram: [ESP32IO relay tutorial](https://esp32io.com/tutorials/esp32-relay)

External reference images are labelled illustrative. They are not represented as the exact HomeFlow board, relay module, or circuit assembly.

## Firmware facts from the supplied sketch

| Appliance | GPIO | ON route | OFF route |
|---|---:|---|---|
| Lamp | 27 | `/lamp/on` | `/lamp/off` |
| Speaker | 26 | `/speaker/on` | `/speaker/off` |
| Coffee machine | 25 | `/coffee/on` | `/coffee/off` |

- Platform: ESP32 using Arduino IDE / Arduino C++.
- Network: ESP32 joins the configured Wi-Fi network.
- Server: `WebServer server(80)`.
- Relay logic in the supplied code: `LOW` = ON and `HIGH` = OFF.
- Each handler returns an HTTP 200 plain-text response.
- Wi-Fi credentials are intentionally not included in public source.

The supplied firmware excerpt documents manual ON/OFF control. The website screenshot shows Timer and Schedule navigation, but timer/scheduling logic was not included in the firmware excerpt. Those features are not described as verified firmware functionality.

## GitHub Pages deployment

1. Open repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/(root)`.
4. Save and wait for deployment.

Expected site URL: https://dhruvkalkeri.github.io/HomeFlow/

## Safety

The wiring diagram is a general educational reference, not the verified HomeFlow schematic. Do not copy mains wiring blindly. Confirm relay ratings, isolation, enclosure, fusing, supply requirements and AC wiring with a qualified person.
