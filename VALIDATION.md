# Validation and limits

Test environment: Webots R2025a on Linux, Python controller, software OpenGL.

The flight test runs the workshop controller with scripted keyboard events through Webots' external-controller TCP connection. The distributed project uses the normal local controller setting. Scripted events exercise the same movement and identification logic used by the keyboard.

Checks cover physical takeoff, position hold, travel to the red, green and blue blocks, camera colour at each block, and the found counter reaching three. This is a simulation test, not a real DJI flight test. The controller uses the model's motors, IMU, GPS and gyroscope. It changes the robot's pose directly only for the N restart action.

Literal model and texture references were checked for missing files. Python syntax was checked. The presentation undergoes package and layout validation.

Limits: the controls have not been manually tested on macOS or Windows here. The automated mission keeps the initial heading and height, so manual Q/E turning, W/S height changes and N restart need a facilitator rehearsal. Performance varies by graphics hardware. The controller bounds requested horizontal positions to the clear practice area.

After the flight-test source was generated, the final controller received a readiness latch so that lowering the drone below the takeoff threshold does not disable the controls. A separate logic check verified readiness persists at low altitude and clears on restart. The physical mission stays at about 3 m, where the behaviour is unchanged.

Manual identification checks proximity and level attitude after the participant presses R, G or B. It does not run automatic image recognition. The camera images in the presentation come from the simulated camera.

Final overlay text uses dark navy for readability on the grass. Test screenshots show the earlier white overlay text.
