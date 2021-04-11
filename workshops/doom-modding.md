### 4.11.2021 Doom-Modding Workshop

**NOTE: this is an automated translation from PDF to TEXT** of the [PDF SETUP file from the workshop](2021_FEED_Doom_Workshop_SETUP.pdf)


### Led by Eben Kling & Aude Jomini (FEED)


```
audejomini@gmail.com Instagram: @audehelene
kling.eben@gmail.com @ebenkling
https://www.ebenkling.com/ @feedfeednhv
http://www.feedfeednhv.com
```
```
TWITCH link: https://www.twitch.tv/audehelene
```
When DOOM was created and released in 1993 its creators were strong proponents of copyleft and free remix culture. A
year later the first shareware level editing and game modding software was released. The beauty of Doom is its
continued accessibility, the speed of the game and its thriving community of sharing knowledge online. It is still fast and
fun, with instant multi-player potential, and we still love to play. With recent improvements through ZDoom, higher
resolution images allow improved possibilities for creative storytelling. We want to encourage other artists to make
worlds in it too.

### About us, and why Doom?

We are not experienced coders or software engineers: we are painters and architects. We have been making work with
_Doom_ during COVID to express our ideas about digital identity, void-like architecture and public space more directly.
_Doom_ became our site of collaboration for 2020, a complicated love letter to our city. Our game, a conversion mod
called _Doom-Haven,_ is set in Long Wharf and downtown New Haven. Using _Doom_ as a medium has given us a way to
travel back in time while thinking through current issues. Endless _Ports of Doom_ in multitude testify to the game’s
enduring wide reach, as well as its code’s resiliency and continued accessibility. The code and textures live in _“.wad”_
files, named for “ _where is all the data?” Wads_ can be taken apart in their entirety, thus unlocking both the images and
code lumps that make up the game. The back-end builder for maps allows free exploration and fast experimentation
using the engine, allowing for digital travel into a 27 - year repository of other mods. Various enthusiasts have taken up
the mantle of upkeep and have sustained the life of this game for the past 27 years, extending the functionality and
resolution of its building tools. It’s such an awesome world.

### Post your experiments... We would love to see them!

- **_On Instagram: tag us... @feedfeednhv, @babycastles_**
- **_On Itch.io: link to our resource at https://audehelene.itch.io/_**

```
Babycastles Academy is the education arm of Babycastles.
Help keep Babycastles thriving during COVID-19!
Venmo: @babycastles to make a donation or sign up for
a membership at: https://withfriends.co/babycastles
```

## LESSON PLAN AND WORSHOP RESOURCES

Using our own experimental game, Doom-Haven (at [http://www.feedfeednhv.com/digital/index.html)](http://www.feedfeednhv.com/digital/index.html)) we will
show you how to make a game using Slade and DoomBuilder, including scripting in Decorate and ACS.
We will go over basic tips and map making tricks, share our custom sprites and textures as an asset pack, and
explain multi-player server setup. We will point you to the Doom community resources which helped us most
along the way. The lesson plan and quick-start guide with downloadable resources are outlined below.

## WORKSHOP OUTLINE-----------------------------------------

```
A. Intro & Workshop setup 20 Minutes
```
**1. Mac OS notes
2. Quick-Start Resource Links and Contents
3. Software Setup Overview
4. Install Console using DoomHaven Demo
5. Base Game – Doom2 vs Freedoom
6. Setting Up Modding Tools
B. Resource Links and Overall Game Structure (SLADE)** _5 Minutes_
**C. Overall functions and Basic Map Building (GZDoomBuilder)** _15 Minutes_
a. Bowling Alley Room 1: Basics & Sector building
**D. Importing Textures and Making Actors (SLADE)** _15 Minutes_
a. TEXTURES for UDMF
b. custom assets and DECORATE
c. Interfacing with the map editor
**E. More details on Map Building (GZDoomBuilder)** _50 Minutes_
a. Room 2: Texturing and Offsets
b. Room 3: Doors, Lifts, 3D Floors & Bridges
c. Room 4: Switches, Lighting, Fog, and ACS scripting
d. Room 5: The newsstand....Final words
**F. !Leave you mailing address here to receive our free art newspaper!
https://forms.gle/sHmxG1gNo4WjfPPz**

## STEP BY STEP SETUP & LESSON PLAN-------------------------

**1)** *MAC-OS ONLY USERS **:** **_GZDoomBuilder_** **does not have a** **_MacOs_** **compatible release...**

#### OPTIONS:

- Run Windows using **Parallels** : free 14-day trial https://www.parallels.com/products/desktop/trial/
- Run Windows using **BootCamp:** https://support.apple.com/boot-camp
- Use **Slade** for map editing-- (a bit more limited functionality, but it works!)

### Tutorials and Intro to SLADE Map Editing in UDMF can be found here:

```
http://slade.mancubus.net/index.php?page=wiki&wikipage=Tutorials
```

#### 2) QUICKSTART RESOURCE:

### a. WINDOWS DOWNLOAD:

**_https://drive.google.com/file/d/1iCVWe6zWVB7R_cm2Z5ZlYxygLZ74JIfm/view?usp=sharing_**

### b. MAC-OS DOWNLOAD *:

**_https://drive.google.com/file/d/1kNfQ7GuxdnrzfYd5fKXyNNaip2KfWKBw/view?usp=sharing_**

- WHAT IS INCLUDED:
    - **One click installer for Console + Our demo Game:**
       **a. GZDoom**
       **b. Free base game:**
          i. FreeDoom2 (modified version)
       **c. Bonus: Doom-Haven Demo game**
    - **Game Editing Tools:**
       **_a._** **GZDoomBuilder (** **_Windows Only)_**
       **b. Slade**
    - **Custom Workshop Assets:**
       **a. Workshop Map:**
          i. DoomBowling.wad
       **b. Workshop assets:**
          i. **DoomHaven_Demo01.wad** asset pack includes:
             1. Custom Sprites (FEED)
             2. Custom Textures (FEED w/ Layet Johnson & Phil Lique)
             3. Custom HUD graphics & Tools (FEED)
             4. Custom Sounds (by Nick Grunerud, Nate Lerner)

#### 3) SOFTWARE SETUP OVERVIEW

- Download Workshop Starter Pack with all resources
- Use DoomHaven Demo installer for quickest setup
- Installing the Base Game separately
    o Doom2 vs FreeDoom
- GZDoom Console
    o Console Setup
    o Test the game
- Install modding tools
    o Slade
    o GZDoomBuilder
- **_Optional_** : (if you are new to writing code) Add code editor software:
    - Free Options below, library for ACS here https://forum.zdoom.org/viewtopic.php?t=
       1. Notepad++ (PC) https://notepad-plus-plus.org/downloads/
       2. Brackets (for Mac) [http://brackets.io/](http://brackets.io/)


#### 4) DOOM HAVEN DEMO = ONE CLICK CONSOLE INSTALL

- Use our **DoomHaven Demo installer** for a quicker start:
- Double Click and go through the prompts.
    o This will install **GZDoom Console** + a **modified Freedoom base game file**
    o BONUS: you also get our DoomHaven demo game.
       ▪ More info about our process and game here:
          [http://www.feedfeednhv.com/digital/index.html](http://www.feedfeednhv.com/digital/index.html)
- Test if **GZDOOM** works by double clicking and playing DoomHaven
- This is the default location where console and game resource will install- we will use it later:
    **C:\Program Files (x86)\DoomHaven_Demo\Support_Files**
- Issues: more info on install here: [http://www.feedfeednhv.com/digital/demo01.html](http://www.feedfeednhv.com/digital/demo01.html)

#### GZDOOM GAME CONTROLS FOR DOOM-HAVEN


#### 5) BASE GAME

- **DOOM2 (Steam or Gog.com):** USE IF YOU PREFER TO WORK WITH THE CLASSIC SPRITES & ASSETS!
    - **$4.99** https://store.steampowered.com/app/2300/DOOM_II/
    - **$9.99** https://www.gog.com/game/doom_ii_final_doom

#### OR......

- **FREEDOOM (modified version for this workshop included in starter pack):**
    o Freedoom aims to be compatible with most mods so they can be played without the need to
       use non-free software: it is a free complete replacement base game for Doom.
    o See website: https://freedoom.github.io/index.html

#### 6) GZDOOM CONSOLE SETUP

- **Only the first time:**
    - This console will ask where the base game,
       or “iwad” is located.
    - Navigate either to Doom2 or Freedoom.
- If you bought Doom thru Steam,
    navigate to your Steam Apps at:
    - **C:\Program Files (x86)\Steam\steamapps\**
    **common\Doom 2 \base\doom2.wad**
- If you are using our included free base game,
    navigate to the resource folder and
       - Browse to file called “freedom2.wad”:

```
C:\Program Files (x86)\DoomHaven_Demo\Support_Files
```
- Turn off “ _Fullscreen”_ to avoid issues.
- Latest Builds and dev team info:
https://zdoom.org/downloads


#### 7) SETTING UP MODDING TOOLS:

#### • SLADE SETUP

- **Included in starter pack, or at**
    **https://slade.mancubus.net/index.php?page=downloads**
- **Run this software in Admin mode to avoid issues.**
- **Only the first time:**
- Tell the software where the base game,
or “iwad” is located in Settings.

```
C:\Program Files (x86)\DoomHaven_Demo\Support_Files
```
- **You can use this software to edit Maps on MacOs.**
- **Open any WAD or PK3 mod you find on the web,**
- **including the base doom2.wad: Exports any assets as PNGs and sounds as WAV.**


#### • GZDOOMBUILDER SETUP

- **Included in the resource**.
    For latest builds & dev team info:
    **https://devbuilds.drdteam.org/doombuilder2-gzdb/**
- **Install both GZDoomBuilder and GZDB Prerequisites.**
    - **_This may require Windows restart_**
    a. Open GZDoomBuilder as Administrator
    **b. NAVIGATE TO: Tools\Game Configurations**

```
c. If you bought Doom thru Steam, browse to your Steam Apps--likely at:
C:\Program Files (x86)\Steam\steamapps\common\Doom 2\base\doom2.wad
d. If you are using our included free base game, browse to this folder again
C:\Program Files (x86)\DoomHaven_Demo\Support_Files
e. Add “freedom2.wad”. Add this as your base resource if you don’t have real Doom from Steam.
f. Add “DOOMHAVEN_DEMO01.wad”. These are our combined custom assets, which we will be
using to build everything. Or you can use original doom items instead, if you prefer.
```
```
g. In “ NodeBuilder” settings , Use ZDBSP – UDMF Normal
h. In “Testing” settings, Navigate to where you installed GZDoom, likely at
C:\Program Files (x86)\GZDoom\gzdoom- 4 - 3 - 3 - Windows-64bit\gzdoom.exe
i. Check out “ Controls” in settings to see what all the HOT-KEYS are. See P13 of this PDF.
```

#### 8) LET’S BOWL!

#### NOW FULLY SETUP FOR BUILDING AND TESTING!

# (ᄎ)(ᄎ)(ᄎ)(ᄎ)(ᄎ)(ᄎ)(ᄎ)(ᄎ)

```
Follow along with us as go over how to make new assets and maps.
```
## Open the resources below on the web to look up script functions as you go.

#### 9) SCRIPTING AND CODE RESOURCES

## https://zdoom.org/wiki/Main_Page

**See appendix PDFs: list of ACS functions, action specials, and decorate classes.**

- **ACS**
    o **https://zdoom.org/wiki/ACS**
- **DECORATE**
    o **https://zdoom.org/wiki/DECORATE**


## ADDITIONAL RESOURCES---------------------------------------

#### SINGLE-PLAYER MULTI-MOD CUSTOM SETUP:

- **ZDL with GZDoom : Use ZDL to setup multi-wad sessions
and save custom settings**
    **https://zdoom.org/wiki/ZDL**

_MULTI-PLAYER SETUP:_

- **Zandronum Console:** best console for multi-player server games. Test your mod first!*
- **DoomSeeker** : browser for accessing servers to run Zandronum online games
    https://zandronum.com/

#### FREE SERVER HOSTING FOR MULTIPLAYER:

**The Sentinel’s Playground:** Free server setup for zandronum-compatible mods

```
https://allfearthesentinel.net/
```
```
* Warning : Some GZDoom features are not supported on Zandronum. Slopes and very high resolution UDMF
textures can cause issues and must sometime be coded differently. Some code needs to be adjusted.
```

## COMMUNITY & LEARNING--------------------------------------

**Most useful and relevant websites:**

- **Zdoom FORUM**!
    o Ask any question....chances are, it’s already answered **https://forum.zdoom.org/**
- **DoomWiki:**
    o **https://en.wikipedia.org/wiki/Id_Tech**
    o **https://zdoom.org/wiki/Main_Page**
    o **https://zdoom.org/wiki/ACS**
- **ModDB:** Find any mod to learn from **https://www.moddb.com/**
- **DoomWorld: https://www.doomworld.com/**

**Some of our favorite resources:**

- **Decino’s YouTube Channel https://www.youtube.com/channel/UCJ8V9aiz50m6NVn0ix5v8RQ**
    Our favorite resource for how stuff works in Doom, and a showcase for other mods.
- **Chubzdoomer’s YouTube Tutorials https://www.youtube.com/playlist?list=PLCE835098C82D8F**
- **LazyGamer: great GZDoomBuilder Tutorials https://www.youtube.com/channel/UCt3yHgnR9YlO4qXItX03-FA**
- **Realm667** : great for free assets, textures, monsters and objects. Also a repository of tutorials.
    **https://www.realm667.com/index.php/en/**


## FANDOM, OTHER MODS-----------------------------------------

**Some great examples other wads:**

- **Ancient Aliens** : An entirely new Doom game which still uses all the original sprites.
    - Amazing map designs which feel like classic Doom, with a stunning new soundtrack.
    - Great use of linedefs to make level architecture: See **Map 24, “Culture Shock”**
    - **https://www.doomworld.com/forum/topic/87784-ancient-aliens-final-version-on-idgames/**
- **Adventures of Square** : total replacement i-wad
    - **[http://adventuresofsquare.com/](http://adventuresofsquare.com/)**
- **Pirate Doom** : lovingly dressed up demons...
    - **https://www.moddb.com/mods/pirate-doom**
- **Sonic Doom** : different use of the platform
    - **https://www.srb2.org/**
- **Chex Quest** : the first infamous game to be included in a cereal box... It’s a terrible mod...and funny.
    - **https://www.moddb.com/games/chex-quest/**
- **Nuts 3 .wad** : joke wads to crash your RAM are a different genre...
    - **https://www.wad-archive.com/wad/NUTS3-WAD-Triple-the-Nut-Double-the-Mongoose**
- **The Sky May Be:** this is a whole other category of weird...
    - **https://doom.fandom.com/wiki/The_Sky_May_Be**
- **“Top 10” Infamous wads:**
    - **https://doom.fandom.com/wiki/Top_10_Infamous_WADs**
- _DOOMWORLD’S CACOWARDS:_
    - _YEARLY AWARD!!! ENTER YOURS!!!_
    - **https://www.doomworld.com/cacowards/**


## SOME GZDOOMBUILDER HOTKEYS----------------------------

See Settings/Preferences for all Hot-Keys or remapping

```
Action Key Action Key
Visual 3D Mode 퐐^ EDIT Panel 퐑퐢퐠퐡퐭^ 퐁퐮퐭퐭퐨퐧^
Toggle selection Highlight 퐇 Paste Offsets 퐒퐡퐢퐟퐭+퐕
Toggle Info Panel ~ Paste Texture M Button
Script Editor 퐅ퟏퟎ Toggle Visual Vertices ALT+V
Toggle Grid 퐀퐋퐓+퐆 Grid Decrease, Increase ] [
Toggle Event Lines 퐈 Deselect All, Select All(toggles) SHIFT+LEFT Button
Clear Selection 퐂 Navigate in Visual Mode: E,S,D,F
Copy Selection, Texture 퐂퐓퐑퐋+퐂 Select Similar ALT+LEFT Button
Map Options F2 Flip LineDef Direction F
Select 퐋퐞퐟퐭 퐁퐮퐭퐭퐨퐧 Select Bounding Box (thing) E
Copy Properties 퐂퐓퐑퐋+퐒퐇퐈퐅퐓+퐂 Move Thing Right Button (hold)
Fit To Screen HOME Select
```
## USING INHERITANCE---------------------------------------------

https://zdoom.org/wiki/Using_inheritance

## ID NUMBERS FOR CUSTOM SPRITES------------------------------

https://zdoom.org/wiki/Magic_numbers


## !!!THANK YOU FOR PLAYING!!!


```
# Name Category Script Line Engine restriction
0 No special
1 Polyobj_StartLine PolyObjects No script
2 Polyobj_RotateLeft PolyObjects
3 Polyobj_RotateRight PolyObjects
4 Polyobj_Move PolyObjects
5 Polyobj_ExplicitLine PolyObjects No script
6 Polyobj_MoveTimes8 PolyObjects
7 Polyobj_DoorSwing PolyObjects
8 Polyobj_DoorSlide PolyObjects
9 Line_Horizon Renderer No script
10 Door_Close Doors
11 Door_Open Doors
12 Door_Raise Doors
13 Door_LockedRaise Doors
14 Door_Animated Doors
15 Autosave Scripting
16 Transfer_WallLight Renderer No script
17 Thing_Raise Things
18 StartConversation Scripting
19 Thing_Stop Things
20 Floor_LowerByValue Floors
21 Floor_LowerToLowest Floors
22 Floor_LowerToNearest Floors
23 Floor_RaiseByValue Floors
24 Floor_RaiseToHighest Floors
25 Floor_RaiseToNearest Floors
26 Stairs_BuildDown Stairs
27 Stairs_BuildUp Stairs
28 Floor_RaiseAndCrush Floors
29 Pillar_Build Floors and Ceilings
30 Pillar_Open Floors and Ceilings
31 Stairs_BuildDownSync Stairs
32 Stairs_BuildUpSync Stairs
33 ForceField Lines
34 ClearForceField Lines
35 Floor_RaiseByValueTimes8 Floors
36 Floor_LowerByValueTimes8 Floors
37 Floor_MoveToValue Floors
38 Ceiling_Waggle Ceilings
39 Teleport_ZombieChanger Teleporters
40 Ceiling_LowerByValue Ceilings
41 Ceiling_RaiseByValue Ceilings
42 Ceiling_CrushAndRaise Ceilings
43 Ceiling_LowerAndCrush Ceilings
44 Ceiling_CrushStop Ceilings
45 Ceiling_CrushRaiseAndStay Ceilings
46 Floor_CrushStop Floors
47 Ceiling_MoveToValue Ceilings
48 Sector_Attach3dMidtex Sectors No script
49 GlassBreak Lines
50 ExtraFloor_LightOnly Renderer No script
51 Sector_SetLink Sectors
52 Scroll_Wall Scrollers
53 Line_SetTextureOffset Renderer No line
54 Sector_ChangeFlags Sectors
55 Line_SetBlocking Lines
56 Line_SetTextureScale Renderer No line
57 Sector_SetPortal Renderer No script
58 Sector_CopyScroller Sectors No script
59 Polyobj_OR_MoveToSpot PolyObjects
60 Plat_PerpetualRaise Platforms and Lifts
61 Plat_Stop Platforms and Lifts
62 Plat_DownWaitUpStay Platforms and Lifts
63 Plat_DownByValue Platforms and Lifts
64 Plat_UpWaitDownStay Platforms and Lifts
65 Plat_UpByValue Platforms and Lifts
66 Floor_LowerInstant Floors
67 Floor_RaiseInstant Floors
68 Floor_MoveToValueTimes8 Floors
69 Ceiling_MoveToValueTimes8 Ceilings
70 Teleport Teleporters
71 Teleport_NoFog Teleporters
72 ThrustThing Things
73 DamageThing Things
```
**Action specials**

```
Script control
Named scripts
Scripting
Waiting
Math
Information
UDMF
Sounds
Inventory
Display
Level alteration
Actor control
```
```
Break
Continue
Restart
Suspend
Terminate
```
```
ACS_NamedExecute
ACS_NamedSuspend
ACS_NamedTerminate
ACS_NamedLockedExecute
ACS_NamedLockedExecuteDoor
ACS_NamedExecuteWithResult
ACS_NamedExecuteAlways
```
```
ScriptCall
```
```
ACS_ExecuteWait
ACS_NamedExecuteWait
Delay
NamedScriptWait
PolyWait
ScriptWait
TagWait
```
```
Ceil
cos
FixedDiv
FixedMul
FixedSqrt
Floor
Random
Round
sin
Sqrt
StrLen
VectorAngle
VectorLength
```
```
ActivatorTID
CanRaiseActor
CheckActorCeilingTexture
CheckActorClass
CheckActorFloorTexture
CheckActorProperty
CheckActorState
CheckClass
CheckFlag
CheckFont
CheckPlayerCamera
CheckProximity
CheckSight
ClassifyActor
GameSkill
GameType
GetActorAngle
GetActorCeilingZ
GetActorClass
GetActorFloorTerrain
```
```
Contents
```
```
Script control
```
```
Named scripts
```
```
Scripting
```
```
Waiting
```
```
Math
```
```
Information
```
```
Built-in ACS functions
```

**# Name Category Script Line Engine restriction**
74 Teleport_NewMap Exits
75 Teleport_EndGame Exits
76 TeleportOther Teleporters
77 TeleportGroup Teleporters
78 TeleportInSector Teleporters
79 Thing_SetConversation Things
80 ACS_Execute Scripting
81 ACS_Suspend Scripting
82 ACS_Terminate Scripting
83 ACS_LockedExecute Scripting
84 ACS_ExecuteWithResult Scripting
85 ACS_LockedExecuteDoor Scripting
86 Polyobj_MoveToSpot PolyObjects
87 Polyobj_Stop PolyObjects
88 Polyobj_MoveTo PolyObjects
89 Polyobj_OR_MoveTo PolyObjects
90 Polyobj_OR_RotateLeft PolyObjects
91 Polyobj_OR_RotateRight PolyObjects
92 Polyobj_OR_Move PolyObjects
93 Polyobj_OR_MoveTimes8 PolyObjects
94 Pillar_BuildAndCrush Floors and Ceilings
95 FloorAndCeiling_LowerByValue Floors and Ceilings
96 FloorAndCeiling_RaiseByValue Floors and Ceilings
97 Ceiling_LowerAndCrushDist Ceilings
98 Sector_SetTranslucent Renderer
99 Floor_RaiseAndCrushDoom Floors
100 Scroll_Texture_Left Scrollers No script
101 Scroll_Texture_Right Scrollers No script
102 Scroll_Texture_Up Scrollers No script
103 Scroll_Texture_Down Scrollers No script
104 Ceiling_CrushAndRaiseSilentDist Ceilings
105 Door_WaitRaise Doors
106 Door_WaitClose Doors
107 Line_SetPortalTarget Lines
109 Light_ForceLightning Lighting
110 Light_RaiseByValue Lighting
111 Light_LowerByValue Lighting
112 Light_ChangeToValue Lighting
113 Light_Fade Lighting
114 Light_Glow Lighting
115 Light_Flicker Lighting
116 Light_Strobe Lighting
117 Light_Stop Lighting
118 Plane_Copy Sectors No script
119 Thing_Damage Things
120 Radius_Quake Scripting
121 Line_SetIdentification Lines No script
125 Thing_Move Things
127 Thing_SetSpecial Things
128 ThrustThingZ Things
129 UsePuzzleItem Scripting No script
130 Thing_Activate Things
131 Thing_Deactivate Things
132 Thing_Remove Things
133 Thing_Destroy Things
134 Thing_Projectile Things
135 Thing_Spawn Things
136 Thing_ProjectileGravity Things
137 Thing_SpawnNoFog Things
138 Floor_Waggle Floors
139 Thing_SpawnFacing Things
140 Sector_ChangeSound Sectors
145 Player_SetTeam Scripting **(Skulltag only: not supported by ZDoom)**
152 Team_Score Scripting **(Skulltag only:**^ **not supported by ZDoom)**
153 Team_GivePoints Scripting **(Skulltag only: not supported by ZDoom)**
154 Teleport_NoStop Teleporters
156 Line_SetPortal Lines
157 SetGlobalFogParameter Renderer **(GZDoom only: not supported by ZDoom)**
158 FS_Execute Scripting
159 Sector_SetPlaneReflection Renderer **(OpenGL only: not supported by ZDoom)**
160 Sector_Set3dFloor Sectors No script
161 Sector_SetContents Sectors No script
168 Ceiling_CrushAndRaiseDist Ceilings

```
GetActorFloorTexture
GetActorFloorZ
GetActorLightLevel
GetActorPitch
GetActorPowerupTics
GetActorProperty
GetActorRoll
GetActorVelX
GetActorVelY
GetActorVelZ
GetActorViewHeight
GetActorX
GetActorY
GetActorZ
GetAirSupply
GetAmmoCapacity
GetArmorInfo
GetArmorType
GetChar
GetCVar
GetCVarString
GetLevelInfo
GetLineActivation
GetLineRowOffset
GetLineX
GetLineY
GetPlayerInfo
GetPlayerInput
GetPolyobjX
GetPolyobjY
GetScreenHeight
GetScreenWidth
GetSectorCeilingZ
GetSectorFloorZ
GetSectorLightLevel
GetSigilPieces
GetUserArray
GetUserCVar
GetUserCVarString
GetUserVariable
GetWeapon
IsPointerEqual
IsTIDUsed
LineSide
PlayerClass
PlayerCount
PlayerFrags
PlayerInGame
PlayerIsBot
PlayerNumber
SetResultValue
StrArg
StrCmp
StrIcmp
ThingCount
ThingCountName
ThingCountNameSector
ThingCountSector
Timer
UniqueTID
```
```
GetLineUDMFInt
GetLineUDMFFixed
GetSectorUDMFInt
GetSectorUDMFFixed
GetSideUDMFInt
GetSideUDMFFixed
GetThingUDMFInt
GetThingUDMFFixed
```
```
ActivatorSound
AmbientSound
LocalAmbientSound
LocalSetMusic
PlayActorSound
PlaySound
SectorSound
SetMusic
SetMusicVolume
SoundSequence
SoundSequenceOnActor
SoundSequenceOnSector
SoundSequenceOnPolyobj
SoundVolume
StopSound
ThingSound
```
```
CheckActorInventory
CheckInventory
CheckWeapon
ClearActorInventory
ClearInventory
DropInventory
DropItem
GetMaxInventory
GiveActorInventory
```
```
UDMF
```
```
Sounds
```
```
Inventory
```

**# Name Category Script Line Engine restriction**
169 Generic_Crusher2 Ceilings
170 Sector_SetCeilingScale2 Sectors No line
171 Sector_SetFloorScale2 Sectors No line
172 Plat_UpNearestWaitDownStay Platforms and Lifts
173 NoiseAlert Scripting
174 SendToCommunicator Scripting
175 Thing_ProjectileIntercept Things
176 Thing_ChangeTID Things
177 Thing_Hate Things
178 Thing_ProjectileAimed Things
179 ChangeSkill Scripting
180 Thing_SetTranslation Things
181 Plane_Align Sectors No script
182 Line_Mirror Renderer No script
183 Line_AlignCeiling Renderer No line
184 Line_AlignFloor Renderer No line
185 Sector_SetRotation Sectors
186 Sector_SetCeilingPanning Sectors
187 Sector_SetFloorPanning Sectors
188 Sector_SetCeilingScale Sectors
189 Sector_SetFloorScale Sectors
190 Static_Init Sectors No script
191 SetPlayerProperty Scripting
192 Ceiling_LowerToHighestFloor Ceilings
193 Ceiling_LowerInstant Ceilings
194 Ceiling_RaiseInstant Ceilings
195 Ceiling_CrushRaiseAndStayA Ceilings
196 Ceiling_CrushAndRaiseA Ceilings
197 Ceiling_CrushAndRaiseSilentA Ceilings
198 Ceiling_RaiseByValueTimes8 Ceilings
199 Ceiling_LowerByValueTimes8 Ceilings
200 Generic_Floor Floors
201 Generic_Ceiling Ceilings
202 Generic_Door Doors
203 Generic_Lift Platforms and Lifts
204 Generic_Stairs Stairs
205 Generic_Crusher Ceilings
206 Plat_DownWaitUpStayLip Platforms and Lifts
207 Plat_PerpetualRaiseLip Platforms and Lifts
208 TranslucentLine Renderer
209 Transfer_Heights Renderer No script
210 Transfer_FloorLight Renderer No script
211 Transfer_CeilingLight Renderer No script
212 Sector_SetColor Sectors
213 Sector_SetFade Sectors
214 Sector_SetDamage Sectors
215 Teleport_Line Teleporters No script
216 Sector_SetGravity Sectors
217 Stairs_BuildUpDoom Stairs
218 Sector_SetWind Sectors
219 Sector_SetFriction Sectors
220 Sector_SetCurrent Sectors
221 Scroll_Texture_Both Scrollers
222 Scroll_Texture_Model Scrollers No script
223 Scroll_Floor Scrollers
224 Scroll_Ceiling Scrollers
225 Scroll_Texture_Offsets Scrollers No script
226 ACS_ExecuteAlways Scripting
227 PointPush_SetForce Sectors No script
228 Plat_RaiseAndStayTx0 Platforms and Lifts
229 Thing_SetGoal Things
230 Plat_UpByValueStayTx Platforms and Lifts
231 Plat_ToggleCeiling Platforms and Lifts
232 Light_StrobeDoom Lighting
233 Light_MinNeighbor Lighting
234 Light_MaxNeighbor Lighting
235 Floor_TransferTrigger Floors
236 Floor_TransferNumeric Floors
237 ChangeCamera Scripting
238 Floor_RaiseToLowestCeiling Floors
239 Floor_RaiseByValueTxTy Floors
240 Floor_RaiseByTexture Floors
241 Floor_LowerToLowestTxTy Floors
242 Floor_LowerToHighest Floors

```
GiveInventory
SetWeapon
TakeActorInventory
TakeInventory
UseActorInventory
UseInventory
```
```
HudMessage
HudMessageBold
Log
Print
PrintBold
SetFont
SetHudClipRect
SetHudSize
SetHudWrapWidth
SetMugShotState
StrLeft
StrMid
StrParam
StrRight
StrCpy
```
```
ChangeCeiling
ChangeFloor
ChangeLevel
ChangeSky
ClearLineSpecial
QuakeEx
Radius_Quake
ReplaceTextures
SectorDamage
SetAirControl
SetCameraToTexture
SetCeilingTrigger
SetCVar
SetCVarString
SetFloorTrigger
SetFogDensity (GZDoom only: not supported by ZDoom)
SetGravity
SetLineActivation
SetLineBlocking
SetLineMonsterBlocking
SetLineSpecial
SetLineTexture
SetSectorDamage
SetSectorGlow (GZDoom only: not supported by ZDoom)
SetSectorTerrain
SetSkyScrollSpeed
SetUserCVar
SetUserCVarString
SpawnParticle
```
```
CancelFade
ChangeActorAngle
ChangeActorPitch
ChangeActorRoll (GZDoom only: not supported by ZDoom)
CreateTranslation
DamageActor
FadeRange
FadeTo
LineAttack
MorphActor
PickActor
SetActivator
SetActivatorToTarget
SetActorAngle
SetActorFlag
SetActorPitch
SetActorPosition
SetActorProperty
SetActorRoll (GZDoom only: not supported by ZDoom)
SetActorState
SetActorTeleFog
SetActorVelocity
SetAirSupply
SetAmmoCapacity
SetMarineSprite
SetMarineWeapon
SetPointer
SetSubtitleNumber (development version b7bbfd4 (http://zdoom.org/Changelog/b7bbfd4/files) only)
SetThingSpecial
SetTranslation
SetUserArray
SetUserVariable
Spawn
SpawnDecal
SpawnForced
SpawnProjectile
SpawnSpot
SpawnSpotFacing
SpawnSpotFacingForced
SpawnSpotForced
```
```
Display
```
```
Level alteration
```
```
Actor control
```

```
# Name Category Script Line Engine restriction
243 Exit_Normal Exits
244 Exit_Secret Exits
245 Elevator_RaiseToNearest Floors and Ceilings
246 Elevator_MoveToFloor Floors and Ceilings
247 Elevator_LowerToNearest Floors and Ceilings
248 HealThing Things
249 Door_CloseWaitOpen Doors
250 Floor_Donut Floors
251 FloorAndCeiling_LowerRaise Floors and Ceilings
252 Ceiling_RaiseToNearest Ceilings
253 Ceiling_LowerToLowest Ceilings
254 Ceiling_LowerToFloor Ceilings
255 Ceiling_CrushRaiseAndStaySilA Ceilings
256 Floor_LowerToHighestEE Floors
257 Floor_RaiseToLowest Floors
258 Floor_LowerToLowestCeiling Floors
259 Floor_RaiseToCeiling Floors
260 Floor_ToCeilingInstant Floors
261 Floor_LowerByTexture Floors
262 Ceiling_RaiseToHighest Ceilings
263 Ceiling_ToHighestInstant Ceilings
264 Ceiling_LowerToNearest Ceilings
265 Ceiling_RaiseToLowest Ceilings
266 Ceiling_RaiseToHighestFloor Ceilings
267 Ceiling_ToFloorInstant Ceilings
268 Ceiling_RaiseByTexture Ceilings
269 Ceiling_LowerByTexture Ceilings
270 Stairs_BuildDownDoom Stairs
271 Stairs_BuildUpDoomSync Stairs
272 Stairs_BuildDownDoomSync Stairs
273 Stairs_BuildUpDoomCrush Stairs
274 Door_AnimatedClose Doors
275 Floor_Stop Floors
276 Ceiling_Stop Ceilings
277 Sector_SetFloorGlow Sectors
278 Sector_SetCeilingGlow Sectors
279 Floor_MoveToValueAndCrush Floors
280 Ceiling_MoveToValueAndCrush Ceilings
281 Line_SetAutomapFlags Lines
282 Line_SetAutomapStyle Lines
```
Retrieved from "https://zdoom.org/w/index.php?title=Action_specials&oldid=48300"

**This page was last edited on 13 February 2021, at 12:02.**
Content is available under GNU Free Documentation License 1.2 unless otherwise noted.


**Classes:Doom**

This is a list of the default classes available in Doom 1 and 2. For classes from other games, see the main article.

```
Characters
Monsters
Stealth Monsters
The Marines
Explosives
Pickups
Weapons
Ammo
Powerups
Keys
Props
Tech
Hell
Corpse
Gore
Misc
```
```
Arachnotron // Arachnotron
```
ArchvileBaronOfHell // Arch-vile // Baron of Hell (^)
HellKnight // Hell knight
CacodemonCyberdemon // Cacodemon // Cyberdemon (^)
Demon // Demon
SpectreChaingunGuy // Partially invisible demon // Former human commando
DoomImp // Imp
FatsoLostSoul // Mancubus // Lost soul (^)
PainElemental // Pain elemental
RevenantShotgunGuy // Revenant // Former human sergeant (^)
SpiderMastermind // Spider mastermind
WolfensteinSSZombieMan // Former human trooper // Wolfenstein soldier (^)
StealthArachnotron // Stealth Arachnotron
StealthArchvileStealthBaron // Stealth Baron // Stealth Archvile
StealthHellKnight // Stealth Hell Knight
StealthCacodemonStealthDemon // Stealth Demon // Stealth Cacodemon
StealthChaingunGuy // Stealth Chaingunner
StealthDoomImpStealthFatso // Stealth Mancubus // Stealth Imp(Doom)
StealthRevenant // Stealth Revenant
StealthShotgunGuyStealthZombieMan // Stealth Trooper // Stealth Sergeant
MarineBFGMarineBerserk // BFG Marine // Marine (Powerful Punch) (^)
MarineChaingunMarineChainsaw // Chaingun Marine // Chainsaw Marine (^)
MarineFist // Marine (Punches)
MarinePistolMarinePlasma // Pistol Marine // Plasma Gun Marine (^)
MarineRailgun // Railgun Marine
MarineRocketMarineSSG // Super Shotgun Marine // Rocket Launcher Marine
MarineShotgun // Shotgun Marine
ScriptedMarineMBFHelperDog // Marine Best Friend Helper Dog (The dog is not avaliable in programs similar to Zdoom) // Marine (No Attack) (^)

Contents
Characters
Monsters
Stealth Monsters
The Marines
Explosives

```
ArachnotronPlasmaArchvileFire // Fire (This shows the fire prior to the attack) // Arachnotron Plasma Bolt (^)
BaronBallCacodemonBall // Baron/Hell Knight Fireball // Cacodemon Fireball
BFGBallBFGExtra // BFG Plasma Ball // BFG Hit Animation (^)
BulletPuff // Bullet Puff
DoomImpBallFatShot // Mancubus Fireball // Imp Fireball(Doom)
PlasmaBall // Blue Plasma Bolt
RevenantTracerRevenantTracerSmoke // Revenant Missile // Revenant Homing Missile Trail (^)
Rocket // Fired Rocket
BFG9000 // BFG 9000
ChaingunChainsaw // Chaingun // Chainsaw (^)
Fist // Punch (yes thats right)
PistolPlasmaRifle // Pistol // Plasma Gun (^)
RocketLauncher // Rocket Launcher
ShotgunSuperShotgun // Shotgun // Double-barreled Shotgun (^)
Backpack // Backpack (Increase carrying capacity)
CellCellPack // Cell // Cell Pack (^)
Clip // Ammo Clip
ClipBoxRocketAmmo // Box of Bullets // Rocket
RocketBox // Box of Rockets
ShellShellBox // 4 Shells // Box of Shells (^)
AllmapArmorBonus // Computer Area Map // Armor Helmet
Berserk // Berserk Pack (Full Health+Super Strength)
BlueArmorBlurSphere // Heavy Armor // Partial Invisibility (^)
GreenArmor // Light Armor
HealthBonusInfrared // Light-Amp Goggles // Health Potion (^)
InvulnerabilitySphere // Invulnerability
MedikitMegasphere // Medikit(+25 Health) // Megasphere (+200 Health/Armor) (^)
RadSuit // Radiation Suit
SoulsphereStimpack // Stimpack(+10 Health) // Soul Sphere (+100 Health)
BlueCardBlueSkull // Blue Keycard // Blue Skull Key (^)
RedCardRedSkull // Red Keycard // Red Skull Key (^)
YellowCard // Yellow Keycard
YellowSkull // Yellow Skull Key
Column // Mini Tech Light
BurningBarrelExplosiveBarrel // Barrel Fire // Exploding Barrel(Doom) (^)
TechLamp // Large Tech Lamp
TechLamp2TechPillar // Small Tech Lamp // Tech Column
BigTreeBlueTorch // Big Scorched Tree // Large Blue Torch
Candelabra // Candelabra
CandlestickEvilEye // Floating Eye above Candle // Candle (^)
FloatingSkull // Floating Skulls
GreenTorch // Large Green Torch
**Pickups
Weapons
Ammo
Powerups
Keys
Props
Tech
Hell**


HeadCandlesHeadOnAStick // Skulls with Candles // Stick with Impaled Head (^)
HeadsOnAStickHeartColumn // Green Pillar with Heart // Stick with several Impaled Heads
RedTorch // Large Red Torch
ShortBlueTorchShortGreenColumn // Small Blue Torch // Short Green Pillar (^)
ShortGreenTorch // Small Green Torch
ShortRedColumnShortRedTorch // Small Red Torch // Short Red Pillar
SkullColumn // Red Pillar with Skull
StalagtiteTallGreenColumn // Stalagmite (on the ground) // Tall Green Pillar
TallRedColumn // Tall Red Pillar
TorchTree // Small Burned Tree
DeadCacodemon // Cacodemon Corpse
DeadDemonDeadDoomImp // Demon Corpse // Imp Corpse(Doom)
DeadLostSoul // Lost Soul Corpse (If you give it one)
DeadMarineDeadShotgunGuy // Marine Corpse // Sergeant Corpse (^)
DeadZombieMan // Trooper Corpse
GibbedMarineGibbedMarineExtra // Gibbed Marine Corpse // Gibbed Marine Corpse 2 (^)
BloodyTwitch // Twitching Hanging Body
BrainStemColonGibs // Brains // Blood Pool with skin (^)
DeadStick // Dead Impaled Body
GibsHangBNoBrain // Crushed Gibs (Placeable in level editor) // Hanging Body (Missing Brain)
HangNoGuts // Hanging Body (Missing Insides)
HangTLookingDownHangTLookingUp // Hanging Torso looking up // Hanging Torso looking down
HangTNoBrain // Hanging Torso (Missing Brain)
HangTSkullLiveStick // Twitching Impaled Body // Hanging Torso (Exposed Brain)
Meat2 // Hanging Body
Meat3Meat4 // Hanging Body with missing leg // Hanging Torso
Meat5NonsolidMeat2 // Hanging Leg // Hanging Body (Not Blocking) (^)
NonsolidMeat3 // Hanging Body with missing leg (Not Blocking)
NonsolidMeat4NonsolidMeat5 // Hanging Torso (Not Blocking) // Hanging Leg (Not Blocking)
NonsolidTwitch // Twitching Hanging Body (Not Blocking)
SmallBloodPool // Small Blood Pool
BossBrain // Romero Head
BossEyeBossTarget // Spawn Cube Shooter // Spawn Cube Landing Spot (Spawn these before you (^)
spawn the shooter or it won't spit cubes!)
SpawnShotSpawnFire // Spawn Cube // Spawn Cube Teleport Fire (^)
CommanderKeen // Hanging Commander Keen
DoomPlayerDoomUnusedStates // Marine (Player-Controlled) // A placeholder for some Dehacked-only states (^)
Retrieved from "https://zdoom.org/w/index.php?title=Classes:Doom&oldid=42783"

**Corpse
Gore
Misc**
```

