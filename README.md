# DOKAPON KINGDOM RANDOMIZER

## REQUIREMENTS
.NET 7.0 Runtime: https://dotnet.microsoft.com/en-us/download/dotnet/7.0

## HOW TO USE

This randomizer will work with the Wii version of Dokapon Kindom and the PC version of Dokapon Kingdom.
Depending on which version you have, there's different steps to take. You'll want to have a zip archive extracter at the ready. I recommend 7zip.

### For the Wii version:
1) Obtain a dumped Wii copy of Dokapon Kingdom. Preferably legally.
2) Download the Wii/GC emulator, Dolphin. A quick google search should be able to find it.
3) Extract all files from Dokapon Kingdom. Make sure the files are kept in their original filepaths.
4) Copy "GAME.PAC" to where your copy of the Randomizer is located.
5) Run the randomizer. When prompted, make a backup, just in case. Follow the remainder of the steps to fill out what options you want.
6) Once you're done, place the altered "GAME.PAC" back where the original one was with the rest of your Dokapon Kingdom's extracted game files.
7) Search your Dokapon Kingdom's extracted game files for "main.dol". Run that file in Dolphin instead of your dumped copy.

### For the PC version:
1) Obtain a copy of Dokapon Kingdom Connect from Steam. I'm unsure of other potential storefronts that may have it.
2) Download "Connect Mod Installer" and "Yet Another CPK Tool". Both can be found on Github and through some potential google searching. Read their instructions to learn how they work.
3) Drag and drop "Data_eng.cpk" onto "Yet Another CPK Tool" to extract its data.
4) After extraction, search the newly created folders for "stageBase_EN.dat" and copy it to where your copy of the Randomizer is located.
5) Run the randomizer. When prompted, make a backup, just in case. Follow the remainder of the steps to fill out what options you want.
6) Once you're done, move the altered "stageBase_EN.dat" into its own folder, then move that folder to where "Connect Mod Installer" is located.
7) Drag and drop the folder with "stageBase_EN.dat" in it onto "Connect Mod Installer" to install it.

## OPTIONS
- Making a Backup (Boolean):
	This allows you to save a backup of your GAME.PAC file whereever it's located before writing to it.

- Randomizing Equipment (Boolean):
	This allows you to randomize the statistics of Weapons, Shields, and Accessories.
	If enabled, you get the following options:
	- SERIOUSLY Randomize Equipment (Boolean):
		This disregards the normal stats of whatever is being randomized and pulls numbers from a randomly generated table instead, making each item have REALLY fluctuated stats.
	- Equipment Strength Multiplier (Float):
		This multiplies the end result of the stat randomization for all items by a flat value.
	- Weapon, Shield, Accessory Strength Variance (Float):
		These will either drop or increase the stats of each type of item by 0% to the specified percentile value you give it.

- Randomizing Magic (Boolean):
	This allows you to randomize the statistics of Offensive, Defensive, and Field Magic.
	If enabled, you get similar options to Equipment Randomization, but for Magic (obviously).
	- SERIOUSLY Randomize Magic (Boolean):
		This disregards the normal stats of whatever is being randomized and pulls numbers from a randomly generated table instead, making each item have REALLY fluctuated stats.
	- Magic Strength Multiplier (Float):
		This multiplies the end result of the stat randomization for all items by a flat value.
	- Offensive, Defensive, and Field Magic Strength Variance (Float):
		These will either drop or increase the stats of each type of item by 0% to the specified percentile value you give it.

- Randomizing Player Classes (Boolean):
	This allows you to randomize the statistics of Player Classes. (NOTE: Both genders count as different sets of classes! Stats are not distributed equally to both genders!)
	If enabled, you get the following options:
	- SERIOUSLY Randomize Player Classes (Boolean):
		Again, disregards the original values and replaces them with randomly generated ones.
	- Class Stats Strength Multiplier (Float):
		Multiplies the base stats of the player by a flat value. This does not affect your class' carrying capacities or base HP.
	- Class Base Stats, Level-Up Bonuses, Salary, Inventory Capacity Variance (Float):
		These work like the other variance values. I recommend setting these above zero except for the Inventory Capacity Variance since the changes are usually too small to notice. You do you though.

- Randomizing Monsters (Boolean):
	This allows you to randomize Monster statistics.
	If enabled, you get the following options:
	- SERIOUSLY Randomize Monsters (Boolean):
		Disregards the original values and replaces them with randomly generated ones.
	- Base Stats Strength Multiplier (Float):
		Multiplies the base stats of the player by a flat value. Unlike the Player Classes, this DOES affect HP.
	- Base Stats Variance (Float):
		Works like all the other variance values, increasing or decreasing stats up to the listed percentile value.

- Randomize Consumables (Boolean):
	This option allows Consumable Items' prices to be randomized.

- Randomize Shops and Drops (Boolean):
	These randomize the contents of Shops and Loot Spaces/Monster Drop Tables respectively.
	
- Randomize Prices (Boolean):
	This randomizes the price value of all items in the game.
	If enabled, you get the following options:
	- Minimum Price Value (Integer):
		The lowest value an item can cost for purchase.
	- Price Strength Variance (Float):
		Like all other variance values.
	- SERIOUSLY RANDOMIZE Consumable Item Prices (Boolean):
		Only shows up if Consumables are allowed to be randomized.
		This only affects anything you'd obtain that counts as either a Consumable (crystals, spinners, etc) or as a Gift for the King (gemstones, food, etc). It can make things insanely expensive.
	NOTE: Seriously randomizing anything with Random Prices enabled will randomize their prices dramatically.
	
- Allow Exploits (Boolean):
	This allows some exploitable Items to be put into Shops and ignores Loot Space Types in regards to Loot Space Drop Table Randomization.
	- NOT RECOMMENDED for seriously play. If you're playing casually, feel free to abuse it.
	
- Randomized Run Seed (String):
	The seed for the run. Optional. Will generate based on time if you don't supply one.
	
- Save Output Log (Boolean):
	This will output everything that was randomized to an output log. The file will end up varying in size depending on how much you randomize.