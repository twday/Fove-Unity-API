## Fove

#### Types
`EFVR_ClientCapabilities`
+ EFVR_ClientCapabilities.Gaze
+ EFVR_ClientCapabilities.Orientation
+ EFVR_ClientCapabilities.Position

`EFVR_ColorSpace`
+ Auto
+ GammaCorrected
+ Linear

`EFVR_CompositorError`
+ DeviceMismatched
+ DisconnectedFromRuntime
+ ErrorCreatingShaders
+ ErrorCreatingTexturesOnDevice
+ None
+ RuntimeAlreadyClaimed
+ UnableToCreateDeviceAndContext
+ UnableToFindRuntime
+ UnableToUseTexture
+ UnknownError

`EFVR_ErrorCode`

| Code                       | Value | Code                       | Value |
|----------------------------|:-----:|----------------------------|:-----:|
|Code_NotImplementedYet      |  4000 |Hardware_ | 200
|Code_FunctionDeprecated     |  4001 |Hardware_ | 200
|Connection_General          |  1    |Hardware_ | 200
|Connect_ServerUnreachable   |  2    |Hardware_ | 200
|Connect_RegisterFailed      |  3    |Hardware_ | 200
|Connect_RuntimeVersionTooOld|  4    |Hardware_ | 200
|Connect_HeartbeatNoReply    |  5    |Hardware_ | 200
|Connect_ClientVersionTooOld |  6    |Hardware_ | 200
|Connect_DeregisterFailed    |  6    |None                        | 0
|Connect_NotConnected        |  7    |Position_
|Data_General                |  1000 |Position_
|Data_RegisteredWrongVersion |  1001 |Position_
|Data_UnreadableNotFound     |  1002 |Position_
|Data_NoUpdate               |  1003 |Position_
|Data_Uncalibrated           |  1004 |Position_
|Eye_Left_NoDLibRegressor    |  6000 |Position_
|Eye_Right_NoDLibRegressor   |  6001 |Position_
|Eye_CalibrationFailed       |  6002 |Position_
|Eye_LoadCalibrationFailed   |  6003 |


`EFVR_Eye`

#### Classes
`FoveCompositor`

`FoveHeadset`

#### Structures
`SFVR_CompositorTexture`

`SFVR_GazeConvergenceData`

`SFVR_GazeVector`

`SFVR_HeadOrientation`

`SFVR_Pose`

`SFVR_Quarternion`

`SFVR_Ray`

`SFVR_TextureBounds`

`SFVR_Vec2`

`SFVR_Vec3`
