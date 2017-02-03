# FoveInterface

## Variables:
### _FoveEyeCamera_ \_leftFoveEye
Left Eye Camera
### _FoveEyeCamera_ \_rightFoveEye
Right Eye Camera

## Structures
### FoveInterface.EyeRays
Structure that holds data about eye raycasts
#### _Ray_ EyeRays.left
Raycast from the Left eye
#### _Ray_ EyeRays.right
Raycast from the right eye

## Methods:
### [*Fove.EFVR\_Eye*](Fove.md/#efvr_eye) CheckEyesClosed()
Check whether either of the users eyes are closed
### _bool_ CheckSoftwareVersions(out string error)
Checks the current software version. If the software is up to date, the function will return true. Otherwise the function will return false and an error from the [EFVR_ErrorCode list](Fove.md/#efvr_errorcode)
### _string_ GetClientVersion()
Returns the current client version
### [_FoveInterface.EyeRays_](FoveInterface.md/#foveinterface-eyerays) GetEyeRays()
Returns a structure that contains the current raycast from each eye
### _GazeEyeConvergence_ GetGazeConvergence()
Get Gaze Convergence
### [*Fove.SFVR_Pose*](Fove.md/#sfvr_pose) GetLastPose()

### _Camera_ GetLeftEyeCamera()
Returns the camera for the left eye
### _Vector3_ GetLeftEyeVector()
Returns the current vector of the left eye
### _Vector3_ GetNormalizedViewportPosition(Vector3 pos, EFVR_Eye eye)
### _Camera_ getRightEyeCamera()
Returns the camera for the right eye
### _Vector3_ GetRightEyeVector()
Returns the current vector of the right eye
### _Vector3_ GetHMDPosition
Returns the current position of the HMD
### _Vector3_ GetHMDRotation
Returns the current rotation of the HMD
### _string_ GetRuntimeVersion()
Returns the current Runtime version
### _bool_ IsCalibrated()
Returns whether the Headset has been calibrated
### _bool_ IsHardwareConnected()
Returns whether the Headset and Camera are connected
### _bool_ IsHardwareReady()
Returns whether the Headset and Camera are ready
### _bool_ IsLookingAtCollider(_Collider_ col)
Returns whether the User is looking at a specified collider
### _void_ TareOrientation()
### _void_ TarePosition()
