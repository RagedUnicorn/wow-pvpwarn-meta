# PVPWarn
&nbsp;  
![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/pvpwarn_ragedunicorn_love_classic.png)
&nbsp;  
_PVPWarn aims to help the player to hear and see enemy spells cast on himself and also spells that an enemy player resisted or spells that the player himself resisted_

## Providers

[![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/curseforge.svg)](https://www.curseforge.com/wow/addons/pvpwarn)
[![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/wago.svg)](https://addons.wago.io/addons/pvpwarn)


## What is PVPWarn?

PVPWarns goal is to help the player recognizing combat log events in a more visual and acoustical way. PVPWarn can display visual and acoustical cues when a certain event is found in the combat log. As an example PVPWarn might play a sound both when an enemy warrior activates recklessness and when it runs out.

## Issues

[![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/issues_classic.svg)](https://github.com/RagedUnicorn/wow-classic-pvpwarn/issues) **Classic**

[![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/issues_bcc.svg)](https://github.com/RagedUnicorn/wow-bcc-pvpwarn/issues) **Burning Crusade Classic**

## Source

[![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/source_classic.svg)](https://github.com/RagedUnicorn/wow-classic-pvpwarn) **Classic**

[![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/source_bcc.svg)](https://github.com/RagedUnicorn/wow-bcc-pvpwarn) **Burning Crusade Classic**

## Features of PVPWarn

### Warning

The basic feature of warning the player can be configured for each class and some additional categories such as items, racials and misc.

![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/pvpwarn_configure_spell.gif)

### Avoiding Spells

PVPWarn can also detect when certain spells where either resisted by the player itself or an enemy player.

#### Self Avoid

The avoid tab allows the configuration of warnings for all spells of a certain category. If you're interested in knowing when you resist a certain spells such as the silence of a shadow priest you will configure this in the priest category.

![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/pvpwarn_configure_self_avoid.gif)

#### Enemy Avoid

To configure the resist warning for your own class use the `Enemy Avoid` navigation point. This menu contains all spells for your class that can be resisted and are supported by PVPWarn. If you use a different class the content of that menu is different.

![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/pvpwarn_configure_enemy_avoid.gif)

### Profiles

PVPWarn loads a default profile based on your class when the addon loads for the first time. The default profile can be loaded again at any point. If you however start modifying what spells are tracked you can create a new profile, or you can even have multiple different profiles that you can then load based on your situation.

#### Loading Profiles with Macros

Once a profile is created in can be loaded manually or with a macro.

`/run _G["RGPVPW_MACRO_LOADPROFILE"]("[profileName")`

Example:

`/run _G["RGPVPW_MACRO_LOADPROFILE"]("Warriorprofile")`

### Combat State

PVPWarn can track a targets combat state and will display this next to the targetframe. The combat icon can be moved to another place if required.

![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/pvpwarn_combat.gif)

### Stance State

PVPWarn can track a targets stance state and will display this next to the targetframe.The stance icon can be
moved to another place if required. Tracking the stance is limited to certain classes and can only be tracked if
PVPWarn was able to observe the stance in the combatlog.

![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/pvpwarn_switching_stance.gif)

If PVPWarn is unable to determine the stance it will display a question mark for an icon.

### Enable/Disable Addon in Zones

The addon can be configured to automatically enable or disable in certain zones. This might be useful in Zones such as Alterac Valley where a lot of events are getting generated.

![](https://raw.githubusercontent.com/RagedUnicorn/wow-pvpwarn-meta/master/assets/pvpwarn_configure_zones.jpg)

## FAQ

#### I get a red error (Lua Error) on my screen. What is this?

This is what we call a Lua error, and it usually happens because of an oversight or error by the developer (in this case me). Take a screenshot off the error and create a GitHub Issue with it, and I will see if I can resolve it. It also helps if you can add any additional information of what you were doing at the time and what other addons you have active. Additionally, if you are able to reproduce the error make sure to check if it still happens if you disable all others addons.

#### PVPWarn did not warn me about a certain spell. Why?

This can have multiple errors. It might be an actual bug where the addon did not recognize the spell. Before creating a ticket however please make sure to check that the spell is actually configured to show a visual or acoustical warning.

#### PVPWarn does not support my Spell. What can I do?

PVPWarn is not complete and certain spells might have simply forgotten. If you have a certain spell that you would like to see supported in a future version of the addon make sure to create a ticket for it, and I will have a  look at it.

#### PVPWarn shows me a question mark instead of the stance of the player

This is a limitation of the WoW Api. Stances can only be observed when a warrior is switching from one stance to
another. It is not possible to get infos about the current stance. PVPWarn will however display the stance as soon
as it is able to observe it.