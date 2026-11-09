# Sound Tuner (BETA)

**Sound Tuner** allows you to customize and replace the default propulsion and vehicle sounds in Cities: Skylines II using external .ogg audio files.

Create your own soundpacks, replace individual sounds, and bring a richer audio experience to your city!

## ⚠️ BETA Version Notice

Sound Tuner is currently in **BETA (v0.9+)**.

Core audio interception and custom audio clip loading have been implemented and tested. Some features may still have edge cases or unexpected audio behavior.

Feedback and bug reports are welcome, especially regarding missing sounds, incorrect mappings, or audio clipping.

## ⚙️ Features

*   **Runtime Audio Interception:** Hooks into the game's AudioManager to replace selected vanilla audio clips without modifying savegames.
*   **Custom Soundpacks:** Load external soundpacks through manifest-based audio mapping.
*   **In-Game Settings:** Adjust volume and pitch multipliers for supported sound categories in **Options > Mod Settings > Sound Tuner**.
*   **Automatic Soundpack Discovery:** Detect and load available soundpacks from the designated directory.
*   **Soundpack Framework:** Other creators can develop and distribute their own soundpacks using Sound Tuner as a framework.
*   **Vanilla Sound Fallback:** Missing custom audio files are ignored, allowing the original game sounds to remain in use.

### Supported Sound Categories

Sound Tuner currently supports sound replacement in these three categories:

*   **Subway**
*   **Train**
*   **Car**

More vehicle types and sound categories may be added in future updates.

## 📁 How to Install Custom Audio

Place your custom soundpacks in the following directory:

%USERPROFILE%\AppData\LocalLow\Colossal Order\Cities Skylines II\.cache\Mods\pdx_mods\Sound Tuner\Sounds\Soundpacks\

### Example Soundpack Folder Structure

A soundpack should be organized as follows:

Folder / File

Description

### Example Soundpack Folder Structure

A soundpack should follow this folder structure:

**Soundpack Location**

*   Main directory: Sound Tuner/Sounds/Soundpacks/

*   Example soundpack: Realistic Train Soundpack/


**Required File**

*   manifest.json — Defines the sound mappings for the soundpack.


Local Folder Structure:

\----------Soundpacks

\---------------------------Soundpack Name

\---------------------------------------------------Car

\---------------------------------------------------Subway

\---------------------------------------------------Train

\---------------------------------------------------manifest.json

Modpack Subscription Structure:

\-123456_1

\----------Soundpack Name

\---------------------------Mod.cs and other stuffs

\---------------------------------------------------Car

\---------------------------------------------------Subway

\---------------------------------------------------Train

\---------------------------------------------------manifest.json

**Important**
Each soundpack must contain a manifest.json file that defines its sound mappings.

You can create multiple soundpacks and organize their audio files into the supported category folders. Each soundpack is discovered and loaded separately by Sound Tuner.

Each soundpack must contain a manifest.json file that defines its sound mappings.

You can create multiple soundpacks and organize their audio files into the supported category folders.

Each soundpack should contain a manifest.json file that defines its sound mappings.

You can create multiple soundpacks and organize their audio files into the supported category folders.

### Important

*   Soundpacks must contain valid mappings in their manifest.json file.
*   Missing or invalid audio files are skipped.
*   When a custom sound is unavailable, the game keeps using the original vanilla sound.
*   Custom audio files must use the .ogg format.


## 🔧 Soundpack Creators

Sound Tuner is designed to make custom audio content easier to create and share.

The mod can identify audio-related prefabs and loaded AudioClip names, then generate a file named Available\_Sound\_Keys.txt after the required prefab data has been prepared.

This file is saved in the mod installation directory and on your desktop, making it easier to identify available vanilla sound identifiers when creating soundpacks.

The mod also includes demonstration audio:

*   One train rolling sound.
*   One subway motor sound.

Use these samples as a starting point for creating your own custom audio packs!

## manifest.json
This mod reads manifest.json to apply sounds into game.
Therefore, there's no any additional requirement to make code files except required file to upload on pdx mods platform.
The example of manifest.json is like this, and this will keep change after update.
So, Please check the mod files in "C:\Users\Administrator\AppData\LocalLow\Colossal Order\Cities Skylines II\.cache\Mods\pdx_mods\166306_?"

```{
  "mappings": [
    {
      "category": "Train",
      "file": "train_passenger_engine.ogg",
      "audioKey": "public_transportation_train_engine_loop1"
    },
    {
      "category": "Train",
      "file": "train_freight_engine.ogg",
      "audioKey": "public_transportation_train_engine_loop2"
    },
    {
      "category": "Train",
      "file": "train_carriage_rolling.ogg",
      "audioKey": "public_transportation_train_car_loop"
    },
    {
      "category": "Subway",
      "file": "subway_motor.ogg",
      "audioKey": "public_transportation_subway_engine_loop"
    },
    {
      "category": "Subway",
      "file": "subway_carriage_rolling.ogg",
      "audioKey": "public_transportation_subway_car_loop"
    }
  ],
  "version": 1,
  "name": "Realistic Train Soundpack No.1",
  "sharedFiles": {
    "Car/PassengerCar": "PassengerCar.ogg",
    "Car/Bus": "Bus.ogg",
    "Car/Truck": "Truck.ogg",
    "Train/Electric": "Electric.ogg",
    "Train/Diesel": "Diesel.ogg",
    "Train/Freight": "Freight.ogg",
    "Train/Passenger": "Passenger.ogg",
    "Subway/Electric": "Electric.ogg",
    "Subway/Diesel": "Diesel.ogg",
    "Car/Motorbike": "Motorbike.ogg",
    "Car/Scooter": "Scooter.ogg",
    "Car/City Car": "City Car.ogg",
    "Car/Hatchback": "Hatchback.ogg",
    "Car/Minivan": "Minivan.ogg",
    "Car/Sedan": "Sedan.ogg",
    "Car/Sports Car": "Sports Car.ogg",
    "Car/Pickup": "Pickup.ogg",
    "Car/SUV": "SUV.ogg",
    "Car/Muscle Car": "Muscle Car.ogg",
    "Car/Van": "Van.ogg",
    "Car/Bicycle": "Bicycle.ogg"
  }
}
```

## ❤️ Support Development

Enjoying Sound Tuner?

Your feedback, suggestions, and support help me improve this mod and expand its audio capabilities.

**Help me upgrade Sound Tuner and make our cities sound richer!**

[☕ Support me on Ko-fi](https://ko-fi.com/tuchangi)
