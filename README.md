# RLSkinSwapper
The mod currently uses a console like system, just like in source engine games.
Here's a list of the current console commands (per plugin):



plugin load|unload|reload [pluginname]
bind [key] "[action]" //Binds a key to console action
exec [filename] //Executes the config file in bakkesmod/cfg/[filename].cfg
logkeys 0|1 //Log keypresses to console
writeconfig //When binds are set via console, use this command to make changes permanent (write to config file)
listmaps //Lists all the maps
loadmap [mapname] //Loads a map in freeplay mode
toggleconsole //toggles the console
sleep 0-10000 //wait for x milliseconds before executing rest for commands.
debug player //Prints player info to console
debug ball //Prints ball info to console
torq X Y Z F //Add spin to the ball for testing stuff (F is forcemode, use 0-6 (0 & 1 work best?))
training_predictball //Draws a line where the ball is predicted to go (is toggle)
training_scoring 0|1 //Allow goal scoring in freeplay or not
boost set|add|remove unlimited|limited|0-100 //enable/disable unlimited boost, or add, remove or set boost. NOTE: when setting boost to a certain amount, unlimitedboost wil automatically be disabled
respawnboost //respawns the boostpads on the field
alias aliasname "action" //create an alias for an action
gamespeed 1 //Speed of the game, between 0.01 and 10
[TrainingPlugin (enabled)]
ball location|velocity X Y Z
ball stop|reset
player location|velocity X Y Z
player stop|reset
player rotation PITCH YAW ROLL
[Training plugin]
shot_load shotname //load the shot
shot_generate //generates a shot from the loaded shot
shot_reset //Shoots the generated shot
shot_countdowntime //The countdown in seconds (when in striker training)
shot_waitbeforeshot //Time between setting ball & player at location and executing the shot
shot_mirror 0|1 //Allow the shot to be mirrored automatically
[RedirectPlugin (enabled)]
//also works for passes & off the wall clears, play around with these. The default values are the ones I think work the best for passes/off the wall jumps and backwall clears
redirect_shot_speed 0-2000 [1000]//Speed to shoot at
redirect_pass_offset 0-5000 [50] //Offset x & y for passes
redirect_pass_offset_z 0-3000 [200] //height offset
redirect_shoot //Shoots the ball towards you using the above cvars
redirect_on_ground 0|1 //Shoot the ball over the floor
redirect_pass_predict 0|1 //Predict where the player will be when the ball arrives at the player
[ReboundPlugin (enabled)]
//Plugin for getting better at rebounds
rebound_shotspeed 0-2000 [780]
rebound_addedheight 0-2000 [300]
rebound_side_offset 0-5000 [0] //Random offset to the side (for non above the goal rebounds) Picks randomly.
rebound_shoot //shoots the rebound shot
[DefenderPlugin (enabled)]
defender_shotspeed 0-2000
defender_cooldown 0-99999 [3000] //Cooldown time in milliseconds between shots or after a touch
defender_start //Starts defender training (must be in freeplay already)
defender_stop //Stops defender training
[KickoffPlugin (enabled)]
//Use rookie aerial training
kickoff_load 0 //Go to next kickoff
kickoff_load 1-6 //Load certain kickoff
[TouchMinigamePlugin (disabled)]
touch_start //starts touch minigame
touch_stop //stops touch minigame
.cfg files
You can put console commands in .cfg files. The config.cfg and autoexec will automatically be loaded once the mod is loaded.
ONLY put keybinds in config.cfg, as the file will be overwritten when the "writeconfig" command is executed.
.json shot files
You can put console commands in .cfg files. The config.cfg and autoexec will automatically be loaded once the mod is loaded.
ONLY put keybinds in config.cfg, as the file will be overwritten when the "writeconfig" command is executed.
