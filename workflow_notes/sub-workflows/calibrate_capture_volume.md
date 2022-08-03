# Calibrate Capture Volume

- Available Options-
	- set `charuco square size` (int/float)
		- size of edge of black squares in `mm` 
			- (option to convert from inches?)
- Big button that starts recording
	- while recording:
		- Detect charcuro boards in each camera stream
		- Displays (on screen):
			- Current `charuco corners` visible on screen (i.e. colored dottos drawn on detected points)
			- OPTIONAL - display previously detected corners
				- This will help people get good coverage of each camera
					- i.e. you want to let the system see the charuco points all accross the screen, to make the lens distortion correction better
		- Displays (off screen):
			- Number of charuco corners detected for each stream
			- Number of **shared** views for each camera
				- i.e. for `Camera0` - how many frames are there where there are charuco corners visible for BOTH `Camera0` AND `Camera1`
				- This might want to be a 'self similarity grid', i.e. a table with each camera on the rows and columns, with the count-number of shared views in each cell
		- Once EACH CAMERA has 'enough' shared views with at least one other camera, a thing pops up to say that you have enough data to complete calibration
- When Recording is done:
	- Save videos to `calibration_videos` folder
	- Send video paths to `anipose_calibration` process
- END RESULT - 
	- Calibration data is known, and `[session_id]_camera_calibration.toml` is saved to the session folder
		- OR - maybe save calibration data SEPARATELY from 'session' data? 
			- i.e. maintain separation between recordings for `calibration` and recordings for `motion capture`?
		