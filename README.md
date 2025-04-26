# ALS_Replicated UE 5.5.4 | Blueprint Version | You can use it in both C++ and Blueprint projects.

This is a community-based effort to fully and effectively replicate Advanced Locomotion System v4 which is permanently free on the Epic Marketplace. 

Discussion regarding the replication effort of ALS should take place on the official discord for Advanced Locomotion System here: https://discord.gg/wYYMHFu

<p align="center">
  <a href="https://discord.gg/wYYMHFu"><img src="https://i.imgur.com/LP9bZQj.png"></a>
</p>

This repository will operate on a series of pull requests. You are free to download modify and pull request your modifications in. If it meets with the criteria of effectively replicating the project, it will be reviewed and merged in.

---

The primary objective of this ALS version is to modify the structure for greater flexibility, and to incorporate new features from Unreal Engine 5 for enhanced performance.

## What is that?

This Plugin has been recompiled from version 5.3 to 5.5 (just recompilation, no modifications to the plugin or project structure) and will continue to receive recompilation.

Original 5.3 version:

<p align="center">
  <a href="https://github.com/Cesio137/ALS_Replicated"></a>
</p>

## Are you looking for the C++ version?

C++ version:

<p align="center">
  <a href="https://github.com/ShadowfallStudios/ALS-Community"></a>
</p>

### Bug Reporting Template:

```
**Detailed description of issue**
Write a detailed explanation of the issue here.

**Steps To Reproduce:**
1: Detailed Steps to reproduce the issue 
2: Clear steps
3: Etc

**Expected Results:**
A description of what should happen.

**Actual Results:**
A description of what actually happens.
```

# Setting Up Your Project

- Clone the repository or download the latest release.

- Move `ALS_Replicated` folder into your project's `Plugins` folder

- Add the lines below into your `DefaultEngine.ini`, below `[/Script/Engine.CollisionProfile]` tag (Create the tag if it doesn't exist):
  
  ```
  +Profiles=(Name="ALS_Character",CollisionEnabled=QueryAndPhysics,bCanModify=True,ObjectTypeName="Pawn",CustomResponses=((Channel="Visibility",Response=ECR_Ignore),(Channel="Camera",Response=ECR_Ignore),(Channel="Climbable",Response=ECR_Ignore)),HelpMessage="Custom collision settings for the capsule in the ALS_BaseCharacter.")
  +DefaultChannelResponses=(Channel=ECC_GameTraceChannel2,DefaultResponse=ECR_Block,bTraceType=True,bStaticObject=False,Name="Climbable")
  ```