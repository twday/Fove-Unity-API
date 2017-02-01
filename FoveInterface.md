## FoveInterface

#### Variables:

`FoveEyeCamera _leftFoveEye`- Left Eye Camera

`FoveEyeCamera _rightFoveEye` - Right Eye Camera

`FoveInterface.EyeRays` - structure that holds data about eye raycasts
`Ray EyeRays.left` - Left eye Raycast
`Ray EyeRays.right` - Right eye Raycast

Methods:

`GazeEyeConvergence GetGazeConvergence();` - Get Gaze Convergence

`FoveInterface.EyeRays GetEyeRays();` - Get Raycast for each eye

`Fove.EFVR_Eye CheckEyesClosed();`- Check if eyes are closed

`Vector3 GetHMDPosition`- Get Current Position of the HMD

`Vector3 GetHMDRotation`- Get Current Rotation of the HMD

`Fove.SFVR_Pose GetLastPose()`

`Camera GetLeftEyeCamera()` - Get Camera for left eye

`Vector3 GetLeftEyeVector()` - Get Vector for left eye

`Vector3 GetNormalizedViewportPosition(Vector3 pos, EFVR_Eye eye)`

`Camera getRightEyeCamera()` - get Camera for right eye

`Vector3 GetRightEyeVector()` - get Vector for right eye

`void TareOrientation()`

`void TarePosition()`
