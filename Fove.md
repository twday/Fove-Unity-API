# Fove

## Types
#### EFVR_AlphaMode
| Type   | Value |
|--------|:-----:|
| Auto   |   0   |
| One    |   1   |
| Sample |   2   |

### EFVR_ClientCapabilities
| Type                               | Value |
|------------------------------------|:-----:|
|EFVR_ClientCapabilities.Gaze        |   1   |
|EFVR_ClientCapabilities.Orientation |   2   |
|EFVR_ClientCapabilities.Position    |   4   |

### EFVR_ColorSpace
| Type          | Value |
|---------------|:-----:|
|Auto           |   0   |
|Linear         |   1   |
|GammaCorrected |   2   |

### EFVR_CompositorError
| Code                          | Value | Code                         | Value |
|-------------------------------|:-----:|------------------------------|:-----:|
|None                           |  0    |RuntimeAlreadyClaimed         |  201  |
|UnableToCreateDeviceAndContext |  100  |DisconnectedFromRuntime       |  202  |
|UnableToUseTexture             |  101  |ErrorCreatingShaders          |  300  |
|DeviceMismatched               |  102  |ErrorCreatingTexturesOnDevice |  301  |
|UnableToFindRuntime            |  200  |UnknownError                  | 99999 |

### EFVR_ErrorCode

| Code                         |Value | Code                          |Value |
|------------------------------|:----:|-------------------------------|:----:|
|None                          | 0    |Server_General                 | 3000 |
|Connection_General            | 1    |Server_HardwareInterfaceInvalid| 3001 |
|Connect_ServerUnreachable     | 2    |Server_HeartbeatNotRegistered  | 3002 |
|Connect_RegisterFailed        | 3    |Server_DataCreationError       | 3003 |
|Connect_RuntimeVersionTooOld  | 4    |Server_ModuleError_ET          | 3004 |
|Connect_HeartbeatNoReply      | 5    |Code_NotImplementedYet         | 4000 |
|Connect_ClientVersionTooOld   | 6    |Code_FunctionDeprecated        | 4001 |
|Connect_DeregisterFailed      | 6    |Position_NoObjectsInView       | 5000 |
|Connect_NotConnected          | 7    |Position_NoDLibRegressor       | 5001 |
|Data_General                  | 1000 |Position_NoCascadeClassifier   | 5002 |
|Data_RegisteredWrongVersion   | 1001 |Position_NoModel               | 5003 |
|Data_UnreadableNotFound       | 1002 |Position_NoImage               | 5004 |
|Data_NoUpdate                 | 1003 |Position_InvalidFile           | 5005 |
|Data_Uncalibrated             | 1004 |Position_NoCamParaSet          | 5006 |
|Hardware_General              | 2000 |Position_CantUpdateOptical     | 5007 |
|Hardware_CoreFault            | 2001 |Position_ObjectNotTracked      | 5008 |
|Hardware_CameraFault          | 2002 |Eye_Left_NoDLibRegressor       | 6000 |
|Hardware_IMUFault             | 2003 |Eye_Right_NoDLibRegressor      | 6001 |
|Hardware_ScreenFault          | 2004 |Eye_CalibrationFailed          | 6002 |
|Hardware_SecurityFault        | 2005 |Eye_LoadCalibrationFailed      | 6003 |
|Hardware_Disconnected         | 2006 |
|Hardware_WrongFirmwareVersion | 2007 |

### EFVR_Eye
| Type    | Value |
|---------|:-----:|
| Neither |   0   |
| Left    |   1   |
| Right   |   2   |
| Both    |   3   |

## Classes
### FoveCompositor
FoveCompositor.DisconnectedCompositor() <br>
FoveCompositor.GetCompositor() <br>
FoveCompositor.GetOrCreateCompositor()

### FoveHeadset
FoveHeadset.GetHeadset()

## Structures
### SFVR_CompositorTexture
[__Fove.EFVR_ColorSpace__](Fove.md/#efvr_colorspace) colorSpace <br>
__System.intPtr__ pTexture

### SFVR_GazeConvergenceData
__float__ accuracy <br>
__float__ distance <br>
[__Fove.EFVR_ErrorCode__](Fove.md/#efvr_errorcode) error <br>
__ulong__ id <br>
[__Fove.SFVR_Ray__](Fove.md/#sfvr_ray) ray <br>
__ulong__ timestamp

### SFVR_GazeVector
__ulong__ id <br>
[__Fove.EFVR_ErrorCode__](Fove.md/#efvr_errorcode) error <br>
__ulong__ timestamp <br>
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) vector

### SFVR_HeadOrientation
[__Fove.EFVR_ErrorCode__](Fove.md/#efvr_errorcode) error <br>
__ulong__ id <br>
[__Fove.SFVR_Quarternion__](Fove.md/#sfvr_quarternion) quat <br>
__ulong__ timestamp

### SFVR_Pose
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) acceleration <br>
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) angularAcceleration <br>
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) angularVelocity <br>
[__Fove.EFVR_ErrorCode__](Fove.md/#efvr_errorcode) error <br>
__ulong__ id <br>
[__Fove.SFVR_Quarternion__](Fove.md/#sfvr_quarternion) orientation <br>
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) position <br>
__ulong__ timestamp <br>
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) velocity

### SFVR_Quarternion
__float__ w <br>
__float__ x <br>
__float__ y <br>
__float__ z

### SFVR_Ray
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) direction <br>
[__Fove.SFVR_Vec3__](Fove.md/#sfvr_vec3) origin

### SFVR_TextureBounds
__float__ bottom <br>
__float__ top <br>
__float__ left <br>
__float__ right

### SFVR_Vec2
__float__ x <br>
__float__ y

### SFVR_Vec2i
__No Information Available__

### SFVR_Vec3
__float__ x <br>
__float__ y <br>
__float__ z

### SFVR_Versions
__int__ clientBuild <br>
__int__ clientMajor <br>
__int__ clientMinor <br>
__int__ clientProtocol <br>
__int__ firmware <br>
__int__ maxFirmware <br>
__int__ minFirmware <br>
__int__ runtimeBuild <br>
__int__ runtimeMajor <br>
__int__ runtimeMinor <br>
__int__ tooOldHeadsetConnected
