# Chicken Mod Menu Template
### The First Thing To Do Is, Obviously, Download The ZIP Folder, Then Extract It.
### You Can Then Download `Microsoft Visual Studio 2026` ;
Microsoft Visual Studio 2026 ; https://visualstudio.microsoft.com/downloads/
#### It Is Gonna Ask You For What To Download, Choose The Following Development Method ;
~~~~~
.NET desktop development

WinUI application development

Game development with Unity
~~~~~

## Once I Have The Extarcted Folder And Got Visual Studio Code, What Do I Do?
### Step 1
Open The Folder, `ChickenModMenuTemplate` And Open The File Called `StupidTemplate.sln`, This Should Launch `Microsoft Visual Studio 2026`
### Step 2
Click The Little Arrow Next To `Solution 'StupidTemplate' (1 of 1 project)` Then Click The Arrow Next To, `ChickenMenu`. In There, You SHOULD See Exaclty 14 Thing (Without opening anything else.).
##### What You Should See (In Order) ;
~~~~~
> Dependencies

> Classes

> Menu

> Mods

> Notifications

> Patches

  .gitattributes

  .gitignore

  Directory.Build.props

  Directory.Build.target

  LICENSE

> Plugins.cs

> PluginsInfo.cs

  README.md
~~~~~
## What To Do Next, When I Have Maked Sure  To Have Everythng?
### Step 3
Open The Menu Folder And The Mods Folder.
#### Menu SHOULD Look Like ;
~~~~~
Menu
  Buttons.cs
  Main.cs
  Settings.cs
~~~~~
#### Mods SHOULD Look Like ;
~~~~~
Mods
  > Settings
  Movement.cs
  Safety.cs
  Speedboost.cs
  Visuals.cs
~~~~~
### Step 4
Open The Settings.cs, `Menu\Settings.cs`. There, You Can Customise Your Menu, Only The Colors.
#### Here Are Some Of The Coding You May Use To Modify Menu Colors.
~~~~~
Solid Color:
new ExtGradient { colors = ExtGradient.GetSolidGradient(Color.black) }

Simple Gradient (Fade In Between Two Colors):
new ExtGradient { colors = ExtGradient.GetSimpleGradient(Color.black, Color.white) }

Rainbow Color:
new ExtGradient { rainbow = true }
  
Epileptic Color (random color every frame):
new ExtGradient { epileptic = true }
  
Self Color (Gorilla Player Color):
new ExtGradient { copyRigColor = true }
~~~~~
#### Which Line Is The Menu Colors?
##### Line To Modify ;
~~~~~
Line 33, public static ExtGradient backgroundColor = new ExtGradient { colors = ExtGradient.GetSimpleGradient(Color.blue, Color.purple) };
                                                    Only Change What's After "="
~~~~~
##### If You Use Solid Color Or Simple Gradient, Change `(Color.blue, Color.purple)` At The End, For The Simple Gradient, And `(Color.black)` For The Solid Color. (Only Change What's After The "."! (The Color Name)).
#### Color Possible For The Menu ;
~~~~~
red	    <--- Solid red. RGBA is (1, 0, 0, 1).
green	  <--- Solid green. RGBA is (0, 1, 0, 1).
blue	  <--- Solid blue. RGBA is (0, 0, 1, 1).
white	  <--- Solid white. RGBA is (1, 1, 1, 1).
black	  <--- Solid black. RGBA is (0, 0, 0, 1).
yellow	<--- Yellow. RGBA is (1, 0.92, 0.016, 1), but the color is nice to look at!
cyan	  <--- Cyan. RGBA is (0, 1, 1, 1).
magenta	<--- Magenta. RGBA is (1, 0, 1, 1).
gray	  <--- Gray. RGBA is (0.5, 0.5, 0.5, 1).
grey	  <--- English spelling for gray. RGBA is the same (0.5, 0.5, 0.5, 1).

(You Can Also Add light/dark In Front Of Any Of The Color!)
~~~~~
## How Do I Change The Menu Name And Version?
### Step 5
Open The PluginsInfo.cs (Almost The Last One)
~~~~~
> Dependencies

> Classes

> Menu

> Mods

> Notifications

> Patches

  .gitattributes

  .gitignore

  Directory.Build.props

  Directory.Build.target

  LICENSE

> Plugins.cs

> PluginsInfo.cs <---- This One (Double Click It...)

  README.md
~~~~~
#### In It You SHOULD See Exactly (`Modify As You Like/Want...`) ; 
~~~~~
namespace StupidTemplate
{
    public class PluginInfo
    {
        public const string GUID = "org.Hellcat.gorillatag.ChickenMenu";   <--- org.CHANNEL-NAME.gorillatag.MENU-NAME
        public const string Name = "Chicken Menu V1.0.5";                  <--- Menu Name And Version
        public const string Description = "Mod Menu Made By HELLCATVR.";   <--- Menu Description
        public const string Version = "1.0.5";                             <--- Menu Version
    }
}
~~~~~
