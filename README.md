# Unity XR Hands Sample Project

Unity's `XR Hands` package defines an API that allows you to access hand tracking data from devices that support hand tracking. To access hand tracking data, you must also enable a provider plug-in that implements the XR hand tracking subsystem.

> Note: The XR Hands package is now in release mode

Hand tracking provides data such as position, orientation, and velocity for several points on a user's hand. The following diagram illustrates the tracked points:
![Tracked points of a hand](https://docs.unity3d.com/Packages/com.unity.xr.hands@1.1/manual/images/xrhands-data-model.png)

XR Hands is a package that only provides an API to access hand data from devices that support hand tracking. In order to use that data to interact with UI/3D objects in the scene, Unity's `XR Interaction Toolkit` Package is used. The `XRI` toolkit provides several components such as Interactors, Interactables, etc. through which we are able to setup XR interactions with elements in the scene.

### Interactors
Interactor components handle the actions of hovering and selecting Interactable objects in the world. This component is responsible for creating a list of Interactables (called Valid Target) that it could potentially hover or select each frame.

### Interactables
Interactables are objects in a scene that an Interactor can hover, select, and/or activate.

## Unity Project Setup Steps
1. Create a new 3D Project
2. Add `OpenXR Plugin` (name: `com.unity.xr.openxr`)
3. Add `XR Interaction Toolkit` (name: `com.unity.xr.interaction.toolkit`)
4. Add `XR Hands` (name: `com.unity.xr.hands`)
> Note: Add all packages mentioned above by using the Add package by name option in the Package Manager. This will add the latest versions of each package. Don't install packages manually as it might be a previous version which doesn't support hand tracking.
5. Configure Project Settings (set platform to android, set proper interaction profiles, etc.)
6. Import Hand Visualizer from `XR Hands`
7. Import Hand Tracking demo and Starter Assets from `XR Interaction Toolkit`
8. Go to `Assets > XR Interaction Toolkit > 2.3.0 > Hands Interaction > Runtime` and open `Hands Demo Scene`

If you face any issues, use this project since it is already preconfigured and should only require minimal changes
