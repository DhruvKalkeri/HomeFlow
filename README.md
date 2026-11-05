# HomeFlow — Engineering Project Portfolio

Responsive portfolio documenting the ESP32 HomeFlow project.

## Media
- `assets/images/homeflow-prototype.jpg`: user-supplied prototype photograph.
- `assets/images/homeflow-dashboard.jpg`: user-supplied website screenshot.
- YouTube demonstration: https://youtu.be/DlQpEDiLtm8
- Third-party conceptual relay wiring reference from CircuitDigest is clearly labelled as not the verified HomeFlow wiring.

## Supplied firmware facts
- Lamp: GPIO 27
- Speaker: GPIO 26
- Coffee machine: GPIO 25
- Active-LOW relay control: LOW = ON; HIGH = OFF
- Routes: `/lamp/on`, `/lamp/off`, `/speaker/on`, `/speaker/off`, `/coffee/on`, `/coffee/off`

Wi-Fi credentials are deliberately not published. The supplied firmware excerpt shows manual ON/OFF HTTP routes. Timer/Schedule navigation is visible in the screenshot, but timer logic was not included in the supplied sketch.

## Publish
GitHub repository Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save.

## Safety
The external diagram is conceptual only. Do not copy mains wiring blindly. Verify relay ratings, power supply, enclosure, fusing, isolation and AC wiring with a qualified person.
