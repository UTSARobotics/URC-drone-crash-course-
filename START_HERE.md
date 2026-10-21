# DJI drone workshop: start here

Fly a DJI Mavic 2 PRO model in a simulated outdoor field. Find one red, one green and one blue object. Look through the downward camera and press the matching letter when you hover over an object.

This is a Webots simulation with physical propellers and assisted flight. It does not run DJI firmware or control a real drone. The outdoor scene includes grass, trees, a country house and a dirt track.

## 1. Install before the workshop

- Install Webots R2025a: https://github.com/cyberbotics/webots/releases/tag/R2025a
- Install Python 3. Python 3.11 is a suitable choice. On Windows, select “Add Python to PATH” during installation.
- If Webots cannot find Python, set the Python command in Webots Preferences to your Python 3 executable. On macOS, Preferences may appear under the Webots menu. On Windows/Linux, check Tools > Preferences.
- You do not need pip packages. Webots provides the `controller` module itself.
- On macOS, if the downloaded app is blocked, follow Apple's instructions: https://support.apple.com/en-gb/102445

## 2. Open the workshop

1. Extract the whole ZIP into a new folder. Keep all folders together.
2. Open Webots.
3. Choose File > Open World.
4. Open `DJI_Outdoor_Workshop/webots/worlds/dji_outdoor.wbt`.
5. Start the simulation with the Real-time play button.
6. Click inside the 3D scene so it receives your keyboard presses.
7. Wait about 6–10 seconds of simulation time. The drone takes off automatically. Wait for READY.

You should see a detailed DJI drone, a grass field and a small camera view. The simulation clock must be moving. You do not run the Python file separately.

## 3. Fly

| Key | What it does |
| --- | --- |
| Up / Down arrows | Fly forward / backward relative to the drone's heading |
| Left / Right arrows | Move sideways relative to the drone's heading |
| W / S | Raise / lower the requested height, between 2 and 8 metres |
| Q / E | Turn left / right |
| R / G / B | Identify the red / green / blue object below you |
| N | Return to the launch pad, clear the found objects and take off again |

Use short key presses at first. Release the arrows to slow down and hover. Allow a couple of seconds for the drone to settle. Turning changes which direction counts as forward. Moving the viewing camera with the mouse does not fly the drone.

## 4. Identify all three objects

1. Fly toward a coloured block.
2. Look at the downward camera view.
3. Centre the block and release the arrow keys.
4. Press R for red, G for green or B for blue.
5. Check the Found counter. Continue until Found 3/3 and ALL THREE IDENTIFIED appear.

You must hover within about 1 metre of the matching object and keep the drone reasonably level. Repeated presses on the same colour count only once. This is manual identification: you decide the colour, and the program checks your position. There is no score, ranking or time limit.

## If something does not work

- **Nothing moves:** start Real-time and check that the simulation clock increases. Then click the 3D scene.
- **No drone or wrong scene:** check the filename is `dji_outdoor.wbt`. Open the copy from this new ZIP, not an older workshop folder.
- **No camera view:** right-click the drone and look under Camera Devices > camera. Also check the Overlays menu has camera overlays enabled.
- **Camera shows the launch pad:** wait for takeoff. The camera looks down.
- **Python error:** read the Webots Console. Point the Python preference to Python 3 and reload the world. Do not install a package named controller.
- **An object will not register:** centre it, stop moving, wait, then release and press its colour key again.
- **Drone tipped over or got lost:** press N with the 3D view focused.
- **Slow laptop:** close other heavy apps, reduce the window size or disable shadows in the rendering options. Use Real-time for the workshop. Simulation seconds can take longer than real seconds on a slow machine.

## One-hour session

| Time | Activity |
| --- | --- |
| 0–5 minutes | Explain the task and show the drone |
| 5–15 minutes | Open the project and practise the controls |
| 15–35 minutes | Find and identify the three objects |
| 35–55 minutes | Free practice: participants choose what to try |
| 55–60 minutes | Share observations and finish |

Install Webots and Python before the session. There is no competition. Free practice can include a different visiting order, changing height or practising turns. No extra task is required.

## Facilitator notes

At the starting heading, Up moves toward the red block. World positions are red (5, 0), green (9, 5), blue (2, 10), in metres from the launch pad. Avoid giving everyone a compulsory route. Explain that this exercise practises looking for objects from above, which can support rover scouting. It is a workshop exercise, not a claim about current URC competition requirements.

The presentation is included at the top level of the ZIP. The controller code is in `webots/controllers/dji_workshop/dji_workshop.py`. Bundled model files and textures are in `webots/assets`. Keep them together.
