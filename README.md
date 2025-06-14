Edited for Vive Flow.

# Wave CloudXR Sample Client

Demonstrate how to program with NVIDIA CloudXR SDK for VIVE Focus 3 and VIVE XR Elite headset. You can start to develop your own CloudXR application based on this sample client. 

Below are the instructions to build from source. Alternatively you can find a pre-built APK in the [Releases](https://github.com/ViveSoftware/Wave-CloudXR-Sample/releases) section.

## Requirements
- HTC VIVE Focus 3 or VIVE XR Elite 
- [Wave Native SDK 4.3.0](https://developer.vive.com/resources/vive-wave/download/latest/) or later
- [CloudXR SDK 4.0](https://developer.nvidia.com/nvidia-cloudxr-sdk)
- [Google OBOE SDK 1.5.0](https://github.com/google/oboe/releases/tag/1.5.0)
- Android development environment
  - Android Studio 4.0 or later
  - Android SDK 7.1.1 ‘Nougat’ (API level 25) or higher
  - Android build tools 28.0.3
  - Android NDK 21.4.7075529
  - OpenJDK 1.8n
  
## Build Instructions
1. Download [CloudXR SDK](https://developer.nvidia.com/nvidia-cloudxr-sdk) and [Google OBOE SDK 1.5.0](https://github.com/google/oboe/releases/tag/1.5.0).
2. Put ***CloudXR.aar*** and ***oboe-1.5.0.aar*** in ***[ProjectRoot]/app/libs***
3. Download Wave SDK, extract the zip file and copy the ***repo*** folder to ***[ProjectRoot]***, alongside with ***app*** and ***gradle*** folders (paths can be modified in ***build_sdk.gradle***)
4. You are ready to build.

## Installation & Usage
1. Install CloudXR server on your PC.
2. Build Wave CloudXR Sample Client and install the apk to your headset
3. Modify the IP address in ***CloudXRLaunchOptions.txt*** and push it into ***/sdcard*** of your headset. 
   - Please read [CloudXR Command-Line Options](https://docs.nvidia.com/cloudxr-sdk/usr_guide/cmd_line_options.html#command-line-options) for the format of ***CloudXRLaunchOptions.txt***)
5. Launch the apk to start streaming

## Notes
* The application requires WRITE_EXTERNAL_STORAGE permission to proceed, for loading a config file from sdcard and writing CloudXR logs. 
* If RECORD_AUDIO permission is denied, microphone feature will be disabled.
>The above permission requests will be prompted in-headset on first launch. To install it with permissions granted, use the *-g* flag with *adb install*.
> `adb install -g client.apk`
