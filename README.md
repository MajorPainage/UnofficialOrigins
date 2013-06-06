DayZ Origins community build
============================

All credit goes to Cortez for all the hard work to make this mod available.

<u><b>Tools Required</b></u>
============================

- PBO tool which can be found in the tools folder.
(PBO Manager is the better of the two)


<u><b>Installing Database:</b></u>
============================

- You need to have MySQL version 5.5 and up. Work great on  5.5.31-0+wheezy1 (debian). Older version have problem importing the .SQL file
- Import \sqlfile\dayz_origins.sql into your database

(NOTE: If your having issues installing the functions, and get a message saying you don't have permission to install, you must install the functions as a 'root' user)


<u><b>Installing Files:</b></u>
============================

- Install the latest OA Beta Patch (http://www.arma2.com/beta-patch.php)
- Create a new folder copy the files from the OA folder into it. (This help retains your original files if you have to start over)
- Copy the Addons folder from the Arma 2 folder into the same folder.
- Copy the map (@DayzOrigins) into the same folder. (Downloaded from Dayz Commander or other tool)
- Edit the following files:<br>
--- \dayz_1.origins.tavi\config.cfg<br>
--- \dayz_1.origins.tavi\HiveExt.ini<br>
--- \dayz_1.origins.tavi\BattlEye\BEServer.cfg<br>
--- \MPMissions\dayz_1.origins.tavi\Debug\player_spawn_2.sqf (More Details Below)<br>
--- \MPMissions\dayz_1.origins.tavi\Camera\loginCamera.sqf (More Details Below)<br><br>


<u><b>Editing player_spawn_2.sqf:</b></u>

Look for 'Visit: www.epm-gaming.co.uk' on line 361, 385, and 416, and change it to your own website.


<u><b>Editing loginCamera.sqf:</b></u>

Look for:
<pre>
_welcomeMessage = format["Welcome to EPM Gamings's GB 500 #2 Server %1, Enjoy your stay!",format["%1", name player]];
</pre>

Edit this line.


- Copy all the files from your git download into your folder. (Make sure to maintain the same file structure)
- Install your PBO tool if you haven't already.
- Use the PBO tool to pack the \@dayz_1.origins.tavi\addons\dayz_server folder.
(NOTE:  You can also pack the folder in the MPMissions folder, but it isn't required)


<u><b>Optional Add-Ons</b></u>
============================

<b>Auto Refuelling<b>

To enable auto refuelling:
- Edit \MPMissions\dayz_1.origins.tavi\init.sqf
- Look for:
<pre>
	//Remove the double slashes on the line below to enable auto refuelling
	//[] execVM "Scripts\kh_actions.sqf";
</pre>
- Remove the double slashes to enable the add-on, save and restart the server.
(NOTE:  Folders inside the \MPMissions\ folder don't have to be packed to .pbo format)

<b>DMR Damage Scaling Removed</b>

Edit file: MPMissions/dayz_1.origins.tavi/BASTARDS/fn_damageHandler.sqf<br>
Look at lines 81-88.

If you would like DMR's to have the same damage as they would in cherno
then keep or delete lines that are commented out starting with  "  /* if
(_unit == player) then { "  if you want the new style DMR damage they
uncomment out the code.
