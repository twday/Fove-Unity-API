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
FoveCompositor.DisconnectedCompositor()

#### FoveCompositor.GetCompositor()
[*SFVR_Pose*](Fove.md/#sfvr_pose) GetLastRenderPose() <br>
[*EFVR_CompositorError*](Fove.md/#efvr_compositorerror) Submit( <br>
  &emsp;&emsp;[*EFVR_Eye*](Fove.md/#efvr_eye) whichEye, <br>
  &emsp;&emsp;[*Fove.SFVR_CompositorTexture*](Fove.md/#sfvr_compositortexture) texInfo, <br>
  &emsp;&emsp;[*SFVR_TextureBounds*](Fove.md/#sfvr_texturebounds) bounds, <br>
  &emsp;&emsp;[*Fove.SFVR_Pose*](Fove.md/#sfvr_pose) pose <br>
) <br>
[*SFVR_Pose*](Fove.md/#sfvr_pose) WaitForRenderPose()

#### FoveCompositor.GetOrCreateCompositor()
[*SFVR_Pose*](Fove.md/#sfvr_pose) GetLastRenderPose() <br>
[*EFVR_Compositor*](Fove.md/#efvr_compositorerror) Submit( <br>
  &emsp;&emsp;[*EFVR_Eye*](Fove.md/#efvr_eye) whichEye, <br>
  &emsp;&emsp;[*SFVR_CompositorTexture*](Fove.md/#sfvr_compositortexture) texInfo, <br>
  &emsp;&emsp;[*SFVR_TextureBounds*](Fove.md/#sfvr_texturebounds) bounds, <br>
  &emsp;&emsp;[*SFVR_Pose*](Fove.md/#sfvr_pose) pose <br>
) <br>
[*SFVR_Pose*](Fove.md/#sfvr_pose) WaitForRenderPose()

### FoveHeadset
#### FoveHeadset.GetHeadset()
*void* AssignRayProjectionValues ( <br>
  &emsp;&emsp;[*EFVR_Eye*](Fove.md/#evfr_eye) whichEye, <br>
  &emsp;&emsp;*ref float* l, <br>
  &emsp;&emsp;*ref float* r, <br>
  &emsp;&emsp;*ref float* t, <br>
  &emsp;&emsp;*ref float* b  <br>
) <br>
[*EFVR_Eye*](Fove.md/#efvr_eye) CheckEyesClosed() <br>
[*EFVR_Eye*](Fove.md/#efvr_eye) CheckEyesTracked() <br>
[*EFVR_ErrorCode*](Fove.md/#evfr_errorcode) CheckSoftwareVersions() <br>
[*SFVR_GazeConvergenceData*](Fove.md/#sfvr_gazeconvergencedata) GetGazeConvergence() <br>
[*SFVR_GazeVector*](Fove.md/#sfvr_gazevector) GetGazeVector() <br>
[*Fove.SFVR_Pose*](Fove.md/#sfvr_pose) GetHMDPose() <br>
*float* GetIOD() <br>
[*EFVR_ErrorCode*](Fove.md/#evfr_errorcode) GetLastError() <br>
[*Fove.SFVR_Pose*](Fove.md/#sfvr_pose) GetPoseByIndex() <br>
*Matrix4x4* GetProjectionMatrixLH( <br>
  &emsp;&emsp;[*EFVR_Eye*](Fove.md/#evfr_eye) whichEye, <br>
  &emsp;&emsp;*float* zNear, <br>
  &emsp;&emsp;*float* zFar   <br>
) <br>
*Matrix4x4* GetProjectionMatrixRH( <br>
  &emsp;&emsp;[*EFVR_Eye*](Fove.md/#evfr_eye) whichEye, <br>
  &emsp;&emsp;*float* zNear, <br>
  &emsp;&emsp;*float* zFar   <br>
) <br>
[*SFVR_Versions*](Fove.md/#sfvr_versions) GetSoftwareVersions() <br>
*bool* IsEyeTrackingCalibrated() <br>
*bool* IsEyeTrackingCalibrating() <br>
*bool* IsEyeTrackingEnabled() <br>
*bool* IsEyeTrackingReady() <br>
*bool* IsHardwareConnected() <br>
*bool* IsHardwareReady() <br>
*bool* IsMotionReady() <br>
*bool* IsPositionReady() <br>
[*EFVR_ErrorCode*](Fove.md/#evfr_errorcode) ManualDriftCorrection3D(*Vector3* vec) <br>
*bool* TareOrientationSensor() <br>
*bool* TarePositionSensors()

## Structures
### SFVR_CompositorTexture
[*Fove.EFVR_ColorSpace*](Fove.md/#efvr_colorspace) colorSpace <br>
*System.intPtr* pTexture

### SFVR_GazeConvergenceData
*float* accuracy <br>
*float* distance <br>
[*Fove.EFVR_ErrorCode*](Fove.md/#efvr_errorcode) error <br>
*ulong* id <br>
[*Fove.SFVR_Ray*](Fove.md/#sfvr_ray) ray <br>
*ulong* timestamp

### SFVR_GazeVector
*ulong* id <br>
[*Fove.EFVR_ErrorCode*](Fove.md/#efvr_errorcode) error <br>
*ulong* timestamp <br>
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) vector

### SFVR_HeadOrientation
[*Fove.EFVR_ErrorCode*](Fove.md/#efvr_errorcode) error <br>
*ulong* id <br>
[*Fove.SFVR_Quarternion*](Fove.md/#sfvr_quarternion) quat <br>
*ulong* timestamp

### SFVR_Pose
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) acceleration <br>
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) angularAcceleration <br>
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) angularVelocity <br>
[*Fove.EFVR_ErrorCode*](Fove.md/#efvr_errorcode) error <br>
*ulong* id <br>
[*Fove.SFVR_Quarternion*](Fove.md/#sfvr_quarternion) orientation <br>
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) position <br>
*ulong* timestamp <br>
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) velocity

### SFVR_Quarternion
*float* w <br>
*float* x <br>
*float* y <br>
*float* z

### SFVR_Ray
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) direction <br>
[*Fove.SFVR_Vec3*](Fove.md/#sfvr_vec3) origin

### SFVR_TextureBounds
*float* bottom <br>
*float* top <br>
*float* left <br>
*float* right

### SFVR_Vec2
*float* x <br>
*float* y

### SFVR_Vec2i
*No Information Available*

### SFVR_Vec3
*float* x <br>
*float* y <br>
*float* z

### SFVR_Versions
*int* clientBuild <br>
*int* clientMajor <br>
*int* clientMinor <br>
*int* clientProtocol <br>
*int* firmware <br>
*int* maxFirmware <br>
*int* minFirmware <br>
*int* runtimeBuild <br>
*int* runtimeMajor <br>
*int* runtimeMinor <br>
*int* tooOldHeadsetConnected
