# Phedg1 Studios - Item Drop API Fixes

You can contact me in the modding discord as *@Phedg1*
If you are a fan of my work and would like to support me, I now have a [DONATION LINK](http://paypal.me/Phedg1Studios).
The [SOURCE CODE](https://github.com/Phedg1Studios/ItemDropAPI) for this project is available.

My mods would not be possible without the amazing core developers who made and maintian *BepInEx* and *R2API*. The tools they have created, as well as their forthcoming support in the modding discord, made all the difference in the world. If you have chosen to donate to me, I would ask that you also consider donating to them. None of this would be possible without them.

### TLDR ###
Fixes common issues with *R2API's ItemDropAPI* submodule. Also contains an API to set which items monsters can use.

### R2API Item Drop API Fixes ###
* If the drop list does not contain any items that a particular chest can drop, that chest will no longer be spawned.This also applies to casino chests, equipment drones, lockboxes, multishops, 3D printers, Scavenger backpacks and shrines. This is instead of the chest being spawned but giving no item when opened. 
* If the drop list does not contain any items of a particular tier, that tier will be removed from the drop pool. This applies to chests, casino chests, lockboxes, Scavenger backbacks and shrines. This is instead of chests giving no items when that tier is selected.
* Elite enemies and teleporter bosses are now restricted to only dropping items if they are contained in the drop list.
* Cauldrons and Lunar Buds in the Bazaar Between Time will not be interactable and will not display an item if the drop list does not contain any items of their particular tier.
* Shrine of Cleansing will only spawn if the drop list contains lunar items or equipment AND a pearl.
* The Scrapper will only spawn if the drop list contains scrap and non scrap items of the same tier.
* The Artifact of Command interface are contrained to only showing items that are contained within the drop list.
* The Scrapper interface is constrained to only showing items if scrap of that tier of item is contained in the drop list.
* Updates *ShareSuite* so randomized pickups conform to the drop list.

### MONSTER TEAM ITEMS API ###
* Monsters can only receive items that are contained witin the monster drop list. Applies to Scavengers, Void Fields stage and Artifact of Evolution.

## USING MONSTER TEAM ITEMS API ##
To modify the which items monsters can recieve, add hook using `Phedg1Studios.ItemDropAPI.ItemDropAPI.setDropLists += YOUR METHOD`, and inside that hook update `Phedg1Studios.ItemDropAPI.ItemDropAPI.monsterItems`. `monsterItems` is defined as `List<PickupIndex>`. By default it contains every item the player has unlocked.

## NOTE ##
This mod has a quite a large surface area, meaning it interposes with the base game in many places. Because of this, future updates to the base game are likely to break things. If / when this happens, please reach out to me on Discord and let me know.

## CREDITS ##
** Education **
Ebkr, Harb, iDeathHD, KingEnderBrine

** Support, Suggestions, Beta Testing and Bug Reports **
blazingdrummer, breadguy69, Dragasath, FunkFrog, itλy, pindab0ter, Siponodo, Undead, VoidInsanity

## Changelog ##
** v1.0.1 **

* Removed redunant BiggerBazaar code.

** v1.0.0 **

* Initial Release