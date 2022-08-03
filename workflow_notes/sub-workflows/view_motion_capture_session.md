# View Motion Capture Session

- Load videos from `annotated_videos`
	- Display in similar view window to the `recording` stuff
	- Determine framerate by looking at saved `timestamp` data
	- OPTIONS 
		- show raw videos instead (from `synchronized_videos`)
		- detect and show charuco boards?
		- Show `camera` positions (from `[session_id]_camera_calibration.toml`)
- Load `mediapipe_3d` data and display a 3d skeleton in a 3D OpenGL viewport
- INTERFACE - 
	- Start animation (Play button)
	- Stop animation (Stop button)
	- Frame slider (like, a video)
	- Ability to Select particular sections of the recording AND
		- Export ONLY the data from that section
		- i.e. give User ability to pull out specific parts of a longer recording
		- probably just one clip at a time to start, 
		- eventually would be cool to let them select multiple clips and then export them all at once (saved to folders with same structure as a regular session folder?)