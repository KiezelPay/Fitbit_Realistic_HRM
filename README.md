# Realistic heartrate animation for Fitbit SDK
Shows an HR animation in a Fitbit clockface or app which pulses with the same frequency as the user's actual heart rate and stops when the watch is taken off.

# Usage
1. Copy the file `app/hrm.js` to the `app` folder of your app or clockface.
2. Copy the content of `resources/index.gui` to your own `index.gui` and adapt it to load the HR image of your choice and move it to the place on the screen you want.
3. Copy the image file `resources/stat_hr_solid_48px.png` to your own `resources` folder (or use another image).
4. Import the `app/hrm.js` file in your `app/index.js` with `import * as hrm from "hrm";`
5. Call `hrm.initialize()` somewhere in your `app/index.js`

# Images
Other formats of the heart image to use can be found at https://github.com/Fitbit/sdk-design-assets/tree/master/icons
Make sure to change the image filename in `index.gui` as well when you decide to use another one.

# Battery impact
Only when the display is **on** the heartrate will be read and the animation will run. As soon as the display turns off all activity will stop and it will not have any effects on the battery life anymore.