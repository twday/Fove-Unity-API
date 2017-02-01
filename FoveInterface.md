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
### [_GazeEyeConvergence_](Fove.md/#sfvr_gazeconvergencedata) GetGazeConvergence()
Get Gaze Convergence
### [_FoveInterface.EyeRays_](FoveInterface.md/#foveinterface-eyerays) GetEyeRays()
Returns a structure that contains the current raycast from each eye
### [*Fove.EFVR\_Eye*](Fove.md/#efvr_eye)CheckEyesClosed()
Check whether either of the users eyes are closed
### _Vector3_ GetHMDPosition
Returns the current position of the HMD
### _Vector3_ GetHMDRotation
Returns the current rotation of the HMD
### [*Fove.SFVR_Pose*](Fove.md/#sfvr_pose)GetLastPose()
### _Camera_ GetLeftEyeCamera()
Returns the camera for the left eye
### _Vector3_ GetLeftEyeVector()
Returns the current vector of the left eye
### _Vector3_ GetNormalizedViewportPosition(Vector3 pos, EFVR_Eye eye)
### _Camera_ getRightEyeCamera()
Returns the camera for the right eye
### _Vector3_ GetRightEyeVector()
Returns the current vector of the right eye
### _void_ TareOrientation()
### _void_ TarePosition()
