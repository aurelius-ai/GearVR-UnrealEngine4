# GearVR-UnrealEngine4
A simple game using Unreal Engine 4.11.2 for GearVR

## 1 Introduction

In this tutorial I will be going to develop a simple environment where the first person player can walk around. This game was developed in Mac and should be similar to windows. Please see "Note" where I would be including some important points about the structure and running of the game.

## 2 Requirements

### 2.1 General

1. A 2015 Samsung Galaxy phone i.e. S6, S6 edge, S6 edge+ or Note 5.
2. Samsung Gear VR.
3. Experience with Unreal Engine 4. If you don't have any previous experience, you can go through my tutorial on Unreal Engine 4 [here](https://github.com/akshaybabloo/UnrealEngine_4_Notes)

### 2.2 Mac

**Software**

1. [Unreal Engine 4](https://www.unrealengine.com/dashboard)
2. [Android Studio](http://developer.android.com/sdk/index.html)
3. [CodeWorks for Android](https://developer.nvidia.com/codeworks-android)

**Hardware**

1. A 2015 Samsung Galaxy phone i.e. S6, S6 edge, S6 edge+ or Note 5.
2. Samsung Gear VR.

### 2.3 Windows

**Software**

1. [Unreal Engine 4](https://www.unrealengine.com/dashboard)
2. [Android Studio](http://developer.android.com/sdk/index.html)
3. [CodeWorks for Android](https://developer.nvidia.com/codeworks-android)
4. Samsung drivers

**Hardware**

1. A 2015 Samsung Galaxy phone i.e. S6, S6 edge, S6 edge+ or Note 5.
2. Samsung Gear VR.

## 3 Instillation

### 3.1 Mac

#### 3.1.1 Android Studio

1. Download [Android Studio](http://developer.android.com/sdk/index.html).
2. Open it and move it to `Application`.
3. Open the application and follow the instillation process.
4. Once the instillation process is done open the application and do the follow
  1. Click on `Android Studio -> Preference`
  2. Click on `Appreance & Behavior -> System Settings -> Android SDK` and tick on `Android 5.0.1` and `Android 5.1.1`.

**Installing command line tools**

1. Open `Terminal`.
2. Type `nano .bash_profile` and type the following in it:

  ```shell
  # Android
  export PATH="/Users/<user>/Library/Android/sdk/platform-tools:$PATH"
  export PATH="/Users/<user>/Library/Android/sdk/tools:$PATH"
  ```

  > Note 1: `<user>` should be replaced by your user name.

4. To save press `Control + x` and then press `y`.
3. Restart `Terminal` and type `android` to see if the tools are working.

### 3.2 Enabling Android Developer Options

1. Goto `Settings -> About -> Software Info` and click on `Build Number` **seven** times.
2. Now go back, You should now see `Developer Options`.

  <p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/DevOpti.png" alt="New Project" width="300"></p>

3. Click on `Developer Options` and enable `USB debugging`

  <p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/USBDebug.png" alt="New Project" width="300"></p>

4. Once you connect your phone to the system, it will ask you to confirm the connected computers RSA KEY. Click `Ok` to continue.

### 3.3 Getting device ID

Make sure you have your phone connected to the computer and the `USB debugging` is switched on. Open `Terminal` and type in `adb devices`. This will print of an alpha numeric/numeric key something like this.

```
List of devices attached
1234567891011123	device
```

### 3.4 Downloading `Oculus Signature File (osig)` and placing it in UE

Copy the above number and goto [https://developer.oculus.com/osig/](https://developer.oculus.com/osig/) and paste it in the text field then click on `Download File`. `oculussig_1234567891011123` file will be downloaded.

Move this file to `/Users/Shared/UnrealEngine/4.10/Engine/Build/Android/Java/assets/`

### 3.4 Installing `CodeWorks for Android`

Goto [CodeWorks for Android](https://developer.nvidia.com/codeworks-android) and download the instillation file. Open the downloaded file and follow the instillation steps.

This is what I have installed:

```
The following components are installed:
Android SDK
    +Android SDK Base 24.4.1
    +Android Platform Tools 23.0.1
    +Android Build Tools 23.0.2
    Android 4.0.3 (API 15)
        +SDK Platform 4.0.3
    Android 4.1.2 (API 16)
        +SDK Platform 4.1.2
    Android 4.2.2 (API 17)
        +SDK Platform 4.2.2
    Android 4.3.1 (API 18)
        +SDK Platform 4.3.1
    Android 4.4.2 (API 19)
        +SDK Platform 4.4.2
    Android 5.0.1 (API 21)
        +SDK Platform 5.0.1
    Android 6.0 (API 23)
        +SDK Platform 6.0
        +Intel x86 Atom_64 System Image 23
        +ARM EABI v7a System Image 23
    +Android SDK Support Library 23.1.1
    +Android SDK Support Repository Library 25
Android Toolchain
    +Android NDK 10e
    +Eclipse 4.4
    +ADT 24.0.2
    +Apache Ant 1.8.2
    +Gradle 2.2.1
Developer Tools
    +PerfHUD ES 2.2-0
    +PerfKit 4.5.1
    +Tegra Graphics Debugger 2.1.15335.1729
    +Tegra System Profiler 2.5.2019.4751
    +NVTX 1.0
Middleware/API
    +PhysX 3.3.0
    +OpenCV 2.4.8.2
+Documentation 1R4
```

## 4 Developing a game

Please see my tutorial on [UnrealEngine 4](https://github.com/akshaybabloo/UnrealEngine_4_Notes).

> Note 2: The game developed in this tutorial is only a sample environment generated by UnrealEngine.

## 5 Packing it up for Android

Once you have completed designing the game do the following:

Open `Plugins`

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/Plugins.png" alt="New Project" width="700"></p>

Then, make sure you have enabled the following:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/Plugins1.png" alt="New Project" width="700"></p>


Next open your `Project Settings...`

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/ProjectSettingsMenu.png" alt="New Project" width="700"></p>

Then do the following:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/AndroidPlatform.png" alt="New Project" width="700"></p>

Then do this:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/AndroidPlatform1.png" alt="New Project" width="700"></p>

And then this:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/AndroidPlatformSDK.png" alt="New Project" width="700"></p>
