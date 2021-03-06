>#### 请注意:这个仓库使用Git-lfs 请先Fork 然后在 Clone 不然我的lfs 流量会被用完的！！！
>#### Note:This repository is using Git-lfs. Please fork the repository before cloning.Otherwise,my persional bandwidth will be used up!
>[About-storage-and-bandwidth-usage on GitHub](https://help.github.com/articles/about-storage-and-bandwidth-usage/)

[![license](http://img.shields.io/badge/license-MIT-blue.svg)]()
[![AppVeyor](https://img.shields.io/appveyor/ci/gruntjs/grunt.svg)]()

# Synopsis 
An open source tank game made by Unity3D game engine.

> Panzer War used to be a commercial  mobile tank combat game. However,the developer won't have much time to work on it.So the online servers are stopped,and the game become an open source one.

------------

 ![GameScreenShot](https://github.com/Doreamonsky/Markdown/blob/master/Screenshot.jpg?raw=true)
 

## Installation 
####  Clone
> 1. Install git large file storage [Download git-lfs](https://git-lfs.github.com)
> 2. Fork to your repository and clone from your repository！

*Then open the project with Unity3D (Unity 2017.x)*
#### Build  AssetBundles
>1. Open menu Tools/ShanghaiWindy/Build/SceneBuilder .
>2. Switch platform to your building target.
>3. Click Relaod Cooked Scene Data.
>4. Click Label Assets .
>5. Click Build Sub-Assets.

*Then you can run the game from scene "StartUp"*

## Reference
### Wiki 
WIKI Page on GitHub : [View it](https://github.com/Doreamonsky/PanzerWar/wiki)
### Tutorials 
1.Vehicle Configures in Unity3D
Videos on [YouTube](https://www.youtube.com/watch?v=DK3lQzjhvtE) or  [Bilibili](https://www.bilibili.com/video/av16666019)

## Demo Codes
### Instantiate existing vehicle.
 ![GameScreenShot](https://github.com/Doreamonsky/Markdown/blob/master/Readme/01.png?raw=true)
#### Code
```C sharp
using UnityEngine;

public class illustration : MonoBehaviour {
	void Start () {
	    GameDataManager.OfflineMode = true; // Use offline
	    
        GameObject newVehicle = new GameObject("Vehicle"); 
        TankInitSystem initSystem = newVehicle.AddComponent<TankInitSystem>(); // Add vehicle init system
        initSystem.VehicleName = "T-44"; //Set vehicle name
        initSystem._InstanceNetType = InstanceNetType.GameNetWorkOffline; // Switch vehicle to offline mode
        initSystem.BulletCountList = new int[3]{ //Set Bullet counts 
            35,15,5
        };
        initSystem.InitTankInitSystem(); // Load all data 
	}

}
```

## Contributors
[Wang [Doreamonsky]](http://vk.com/doreamonsky "Wang [Doreamonsky]")

[Kovalenko Vlad](https://vk.com/iso_slacker_yt "Kovalenko Vlad")
