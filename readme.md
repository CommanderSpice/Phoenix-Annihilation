﻿Changelog
========

9.46 → 9.55
XX/XX/2017

Important:
• Renamed widget folder to Widgets_BA (if you want custom widgets, (re)name your widget folder)
• Decay resigned as balancing dev/maintainer
• Doo assigned to redesign Sea
• Lots of things changed, please grant us some time to adjust

Balance changes:
• All Energy and metal prices have been rounded (because buildmenu shows prices)
• Introduced a minimum (slightly larger) buildrange
• Vehicles accelerate faster and slows less when turning + 2% speed increase
• Commander torso turnspeed increased 33% + dgun reloadspeed reduced 10%
• Small (2x2) wreckage dont block movement (this is a modoption you can disable: smallfeaturenoblock)
• T2 bombers are in between current and right before the nerf of ba v7.92 (now better buildtime and cost less energy)
• T1 kbot/veh/air lab got 50% additional buildspeed
• Commanders produce 60% additional energy
• Plasma shields are 50% weaker to non LRPC shots, cost reduced by 20%.
• Vanguard does 20% more damage
• Armmart and cormart (mobile T2 arty) do 15% more damage
• Morties are 10% slower and are a bit less acurate (even more when moving)
• Armvulc and corbuzz cost increased by 40%
• Bertha and Intimidator weapons have 25% more Area-of-Effect
• Decoy commanders have been given same lasers as regular commanders
• Fixed viper overshooting (when aiming at radar dots)
• Fixed flak doing ludicrous damage to ground units
• Air transports don't have collision enabled anylonger, fixes the unload bug
• EMP Missile Launcher: Added one step to the animation to improve it which slighlty increases the time to fire the weapon (around +1.25 second). The projectile speed and accel are still the same. Doo
• Pathing improvement: units wont get stuck in cliffs any longer
• Decoy commanders 8% cheaper + same buildpower as com + added Radar, LLT and AA as buildoptions

Wind:
• Wind generators have a bigger footprint: 4x4 (was 3x3), fan blades wont touch eachother this way
• Wind generators 50% more expensive for 50% more energy production/health/buildtime/storage
• Windspeed gained 50% (but due to price increases: generators wont be more effective)

Sea reworked: Doo
-• Work In Prorgess
Changelog date: 07/12/17
IMPORTANT BALANCE CHANGES:
• Increased T1 shipyards costs +40% and decreased T1 and T2 ships costs 20%.
• Increased Patrol Boats reloadtime (100%), decreased hp 345→275, costs -20% (BEFORE the global costs decrease)
• Added GUN PLATFORM to both factions for 160m/1600e. Available in T1 ship con, t2 engineer and Commander buildmenus.
• Added SEA PLATFORM to both factions for 50m/400e. Available in all buildmenus (t1 and t2 cons, land, sea, air, hover, ships)
• Added Plasma Frigates to both factions for 440m/2000e arm, 480m/2160e core. Available in T1 Shipyard.
		These units stats will be posted separately on our Discord channel when they will be definite for the upcoming version.
• Nerfed construction ship buildpower 50%
• Added T1 Kbot Labs, Vehicle Plants, Aircraft Plants, and Nano Turrets to T1 construction ships.
• Reduced corvette costs for both faction (arm 55%, core 57%) and HP (arm 1900=>780, core 1800=>700) (BEFORE the global costs decrease)
• Guardian, punisher, ambusher and toaster now have increased damages against ships. This was an original feature of Absolute Annihilation, that had been kept in the firsts BA version and had been removed at some point, leaving the guardian/punisher as a hardly useful unit.
	They were also given bonus damages towards commanders (which were already existant on their high trajectory mode, but inexistant on their low traj mode.
	The total bonus damages are: T1 and T2: lowtraj +300 vs comms and light ships, +150 vs heavyships, Hightraj +400 vs comms and light ships, +200 vs heavy ships.

MOVEMENT AND UNIT BEHAVIOUR RELATED (nothing is definite for now so i'll just state the global trend):
• Accelerations are being reworked for slower movestarts (which means decreased acceleration overall). 
	I'm calculating the new accel values as such: Acceleration(elmos/f²) = MaxVelocity(elmos/frame)/(30(frame/s)*TimeToReachMaxSpeed(s)
	In the end, once all the MaxVelocity will be balanced, i'll just have to balance the "TimeToReachMaxSpeed" appropriately. As of now, accelerations for ships are clamped between 2 second and 8 seconds.
• MaxVelocities are being reworked: Globaly, they are being decreased for most ships although some of them might have gained a bit of maxspeed in the end.
• TurnRates were, overall, a bit too high and didnt really fit with the unit's corresponding model. They are being reworked for a more realistic behaviour. We are trying to keep it as enjoyable as possible though, and trying to avoid boring collisions against ground.
• TurnInPlaces: As of now, ALL ships will be able to perform a turn-in-place. This might sound tricky and unrealistic. In reality, they never will turn in place because they will always start accelerating while turning. Also, due to finetuning the TurnInPlaceAngleLimit, we are trying to avoid as much as possible the weird behaviours where a ship brakes in the middle of a fight to turn.
The turninplaceanglelimits have been set between 90 and 140 degrees, depending on the usage made of a unit. 
A destroyer, for exemple, shouldn't brake when firing and trying to perform a 180° to avoid shots. We have set the turninplaceanglelimit to 140 degrees, which is the BA7.20 value from back when it still could perform turninplaces
This function allows all move commands that are under 140 degrees not to trigger any braking. 
If you wan to make a full 180° turn with a brake, directly queue the 180° turn. 
If you don't want it to brake, split the turn into two moveorders < 140degrees each.
This value has been set to 90 for construction ships, 110 for pships, 140 for scouts.
These values might be subject to change to enhance the players' experience and avoid unwanted brakes in a middle of an intense battle.
• BrakeRates: They are calculated with the same formula as the acceleration: BrakeRate(elmos/f²) = MaxVelocity(elmos/frame)/(30(frame/s)*TimeToStop(s)
	As of now, the TimeToStop times are clamped between 0.5 and 1.33 seconds.

MODELS AND ANIMATIONS:
• Battleships and Cruisers model have had their Z-axis scaled up a bit (about a 1.4 factor) to give their model a proper ship-like impression.
	The balance change caused by this new model isn't inexistant. It is kept to a minimal, but the turret placements being slightly different can cause some small changes to their effective range. (IE tower further behind = needs to get a little closer to its target).



(AA) missiles:
• AA missile range increased a tiny bit, but Arm/core defender range increased 15%
• T1 aa: pack0 and sam range increased, missile damage increased slightly and price increased 10%
• Fighters have been given more range due to slower missile speed and missile turnrate 
(old fighter missile range was too short to show missile exhaust effect properly)
• Fighters have been given an a2a and a2g missile, the a2g missile has shorter range


Mod options: (default disabled)
• control victory options: shows info on startup and offers a better scoreboard window
• Added modoption for fixed hitspheres (requires firethroughfriendly enabled)
This replaces hitboxes with correctly sized hitspheres. 
Currently hitboxes are smaller than desired, this was done so that units can somewhat can fire over others
Smaller than desired hitboxes result in missed projectiles or projectiles passing through without hitting

Other:
• All new particle/lighting effects!
• Player Color Palette widget has beed added (rainbow scemed team coloring, toggable via Options)
• Added luamex (lua metal extractor points) functionality for mappers
• Resource bars, Energy Conversion, Wind Display, Com Counter, Rejoin progress integrated into 'Top Bar' widget
• Added Tooltip widget, shows tooltips at mouse cursor location
• Buildmenu: shows metal/energy cost and tooltip on hover
• Buildmenu: could show shortcuts when enabled via Options widget
• Buildspacing shortcuts B and N are now ALT+Z and ALT+X
• Keybinds, commands, changelog, options windows hide with Escape key
• Teamstats widget renamed, simplified, spiced up and has a fixed position (this fixes bugs aswell)
• Added grabinput widget (enable if you have problems with mouse detection in (borderless) window mode)
• Projectiles/explosions/laserbeams can have lighting. 'Lighting Effects' option toggable via options widget. (default enabled)
• Added outline widget, toggable via Options (default disabled)
• Unit textures reprocessed with bigger color range and less grain
• More units have been given a shatter effect on death
• Options: fixed that not all settings remembered their value
• Removed right column on options menu to allow a 3rd column of options
• Bloomshader: prettier and more pronounced, offers 2 levels (modest/heavier) via Options
• Pausescreen changed and darkens screen or decolorizes it when shaders enabled
• Changelog widget: version shortcuts only show for every 10th version number
• GUI background 10% darker
• Spiced up 'Buildbar' and 'Selected Unit Buttons' widgets
• Restyled prestart faction change widget (also scales with resolution)
• Removed 'Allies' label from advplayerslist
• Unit info widget removed
• Removed all old loadscreens, added new ones
• Commands FX widget: improved performance
• Ally Cursors widget: improved performance
• Fixed commander nametags occasionally showing spectator name
• Spiced up the loadscreen progress bar
• Fixed cursor size changing after alt-tabbed to desktop and back
• Fixed glitchy/spiky healthbars-shader on intel gfx and very old cards
• Darken map widget can optionally darken features aswell (trees/wreckages)
• Added "Include buildings in area selections" option via option widget (from Smart Select widget)
• Enemy spotter opacity and unit teamcolor highlight configurable via options widget
• Arm Beamer updates its aim faster when firing
• A few more turrets/barrels get a kickback when they fire
• Fixed unit_stats dps values for beamlaser weapons (dps = damages/beamtime+reloadtime instead of dps = damages/reloadtime). Also changed the minimal reload time to 1/600 instead of 1/30, which caused some weapons with reload times < 0.03 to show wrong dps values. Doo
• Fixed unit_stats dps values for stockpiling weapons (had to apply a 1/30 factor). Doo
• Fixed unit_stats crashes when hovering enemy units. Doo
• Replaced engine info screen (shortcut i) with our own screen
• Changed and fixed some missile models (missile.3do, empmisl.3do) Doo
• Krogoth model scaled down (10%) and bantha model scaled up (5%) without any weapon/cost/HP buff or nerf. Doo
• Fixed some models flare pieces to properly spawn the weapon in the right place -• planning on checking every model i can. Doo
• Renamed a lot of unit id's, so they start with arm/cor and the id fits the name
• Added additional extensive unit description (by PtaQ)
• Increased default player unit limit to 1500
• Removed useless repeat/stop/wait orders from a lot of buildings


9.45 → 9.46
22/09/2016

• Ready/substitute button smaller
• Options: fixed options + added toggles for bloom, UI blur, xrayshader, snow, darken map, command fx
• Options: combined fps/clock/gamespeed, removed advsky toggle, treeview slider, high-res los toggle
• Options: shadows has toggle when shadow quality manager widget is active, else it has a slider
• Options: allows inverse scrollspeed
• Flash tank: stripped burst fire (per turret), now its continuesly firing (no balance change)
• Added modoptions (created by Forboding Angel):
• modoption: controlvictoryoptions (control areas to win game)
• modoption: betterunitmovement (units accelerate/respond faster and turn better)
• modoption: firethroughfriendly (you can fire through allied units)
• modoption: smallfeaturenoblock (you can fire through smaal features/wreckage 2x2)


9.44 → 9.45
19/09/2016

• Fixed Ready/Substitute button
• Discord icon: clicking it makes you say the invite link (so you can click it in lobby)
• Options: Merged fullscreen+window screen edge move options


9.43 → 9.44
18/09/2016

• Added Options widget
• We are on 'Discord' at: discord.gg/aDtX3hW (pregame: above advplayerslist is discord icon)
• Ready/sub button appearance/size change and scales with resolution
• Projectile lights widget has enhanced performance (by roink[vegan])
• fixed: partially built planes being incorrectly recognized as damaged and sent to repair pads
• BA icon quality improved


9.42 → 9.43
08/09/2016

• Advplayerslist: fixed crash when doing /specfullview
• Unit stats: mouseover unit + space works again when no units selected (old behavior)
• Set target (shortcut Y) now doesnt attack ground, ALT+Y will still do that
• Critters dissapear less quickly
• Awards screen scales according to resolution


9.41 → 9.42
11/08/2016

Balance changes:
• marauder(arm t3): build time decreased by 10%, speed increased by 5%
• mobile anti make only 100 energy now (was 200)
• Flying Fortress makes 50 energy (was 0)

Other:
• Fixed big crater size
• Fixed "Com DontBreakCloak" widget
• Stockpiler queues 10 missiles instead of 5
• Unit stats: instead of mousover unit +space, now select unit +space
• Advplayerlist: hides resource bars for dead teams
• Ecostats shows core faction icon again
• Fixed set target functionality
• On button press → release.. for: keybinds info, commands info, changelog, clearmapmarks button, team stats


9.40 → 9.41
06/08/2016

• Added "Idle Builders" widget (disabled by default)
• Fixed critters code (it broke chicken defence not starting on maps with critters)


9.39 → 9.40
04/08/2016

Balance changes:
• Damage of t2 Mobile Artillery vehicles increased by 10%
• Units can walk through landed air units

Other:
• Advplayerlist: added player resource bars + moved trueskill value
• "Ally Resource Bars" disabled and renamed to "Ally Resource Bars (old)"
• Changed cursorsets to: 'old', 'old_150', 'bar', 'bar_133'
• Fixed dead/unresponsive screen area (caused by ally selected units GUI)
• RedUI console: filtered connection attempts and spec desyncs (when its not you)
• "Adv. Unit Marker" renamed to "Unit Marker" and disables when becoming spectator
• Critters no longer block units + will follow commanders when in close proximity


9.38 → 9.39
29/07/2016

Balance changes:
• Decreased LOS/radar accuracy to increase game performance
• Vanguard: Build time decreased by 10%
• Tactical Nuke Launcher: metal cost increased from 804 to 1200

Other:
• Changed cursorsets: old, old_150%, old_200%, bar, bar_150%, bar_200%
• Advplayerlist: fps counter instead of cpu usage
• Advplayerlist: fps/cpu tooltip shows system info
• Advplayerlist: spectator activity alpha's (inactive: 0.4, mouse/keyboard: 0.6 and camera: 0.8)
• Added clearmapmarks button (attached to advplayerlist)
• Added death messages
• Decreased number of critter gulls
• Fixed critters related error spam


9.37 → 9.38
23/07/2016

Balance changes:
• EMP spider have no autoheal anymore and have less hp (950 → 850) + speed was reduced by 10%

Other:
• Fixed missing cloak.wav error spam
• /cursor, now also lists available cursorsets
• Bet widget removed
• Comgate widget removed
• Vignette widget removed


9.36 → 9.37
21/07/2016

• Bugfixes
• Spring v103 compatible 


9.35 → 9.36
09/07/2016

Balance changes:
• Heaps are harder to hit (lower hitbox)
• Fixed "closed viper is hard to hit"
• "Set target" fixes

Other:
• Added BAR's cursorset, change to old one with /cursor
• Anti Ranges: an emp'd anti range ring will be blinking
• Ally cursors: idle spec cursors fade away ex-players (specs) no longer have colored cursor
• Removed SmoothScroll widget
• More death messages
• Comgate effect reimplemented as optional widget
• Less critters (wildlife) on land
• Various changes to make it Spring v102 compatible


9.33 → 9.35
05/03/2016

Balance changes:
• Bladewings are ~10% slower

Other:
• new widget: "BA cmdcolors", disable to load engine defaults
• Unit Stats: based on recent version (more precise)
• A lot more widlife at a lot more maps
• Widlife diminishes when total unitcount gets higher
• Bet frontend: unit betlist offset fix
• Various changes to make it Spring v101 compatible 


9.32 → 9.33
14/02/2016

Balance changes:
• Corpses of some t2 veh and kbots are harder to break

Other:
• All GUI elements can be dragged with rightmouse besides middlemouse (in CTRL+F11 mode)
• Widgets: changelog / commands info / unit info:  scrollable with scrollwheel
• Smart select: default (for new installations) disabled the building filter when mobile units under selection. (toggle with /selectionmode)
• Unit stats: applied scaling according to resolution
• Comcounter same size as wind info
• Added wildlife for a select few maps


9.31 → 9.32
06/02/2016

Balance changes:
• Ground "Anti-Nuke System" energy cost reduced by 10%
• Arm & Core Advanced fusion buildtimes raised ~ 15%
• Corpses of some t1 vehicle and kbots are harder to break
• T2 constructors (kbot, veh, air) cost increased by 20%

Other:
• Added widget "Unit Stats": hover over unit and hold spacebar
• Bet frontend: Stripped some info from a unit bet list
• Minor bugfixes


9.30 → 9.31
01/02/2016

• Bugfix FFA alliance error
• "LOS view" pregame disabled again


9.29 → 9.30
30/01/2016

• "AdvPlayersList": fixed allybutton, you can now unally again via the <3 button
• "LOS view": LOS on when playing, off when becoming spectator (+remebers on luaui relaod)
• "Ally Resource Bars": nwo also shows current m/e values when mouseover player
• "Darken map": added '/mapdarkness #'  wherne # can be a value between 0 and 0.6
• "Ecostats": fixed guishader still being active when playing + minor perf improvment


9.28 → 9.29
22/01/2016

FFA
• Alliances break when one attacks an allied player (both ways)
• Alliances break when you target an ally within a weapon's area-of-effect


9.27 → 9.28
16/01/2016

Balance changes:
• Gremlin (Stealth Tank) • harder to EMP
• Annihilator, Doomsday Machine • damage reduced by 10% (all weapons)
• Re-implement Sniper weapon using "cannon" (was "riffle"). Snipers will not kill each other anymore

Others:
• Added workaround for bug with "camera scroll at the beginning of the game"
• Fixed display of advplayerlist ally button <3 for FFA's


9.26 → 9.27
04/01/2016

• Adv playerlist: shows an ally <3 button when alliances are allowed (when bset option: 'Fixed Alliances: No')
• Pathfinder improvement enabled by default (the one from v9.25)
• Fixed occasional errorspam related to stunned metal/energy storages


9.25 → 9.26
19/12/2015

• Comblast & Dgun Range: more acurate range (takes groundheight in account)
• Adv playerlist: hides spec list as player
• Snow: shows onscreen message pregame (when its snowing)
• GUI shader and map_edge_extension: disabled by default
• Adv playerlist mascotte: click on it to change mascotte type
• Adv playerlist: shows alliances under playername with 0.5 opacity  
   (alliances are only optionally availible in ffa: with /ally #number)


9.24 → 9.25
13/12/2015

• Bugfixes
• Pathfinder improvement (optional, for testing)


9.23 → 9.24
08/12/2015

• Decoy coms dont have real dgun weapon damage anylonger.
• Ally selected units: fixed dead mouseclick area


9.21 → 9.23
05/12/2015

• Ally selected units: disco/large dots bugfix + movable options GUI + auto-scale GUI according to resolution
• Bet Frontend: removed dead mouseclick area when being player + unit bet list sorted by time + keeps working on pause
• Ally resourcebars: slightly larger again on small resolutions
• Added widget: "Bloom shader highlight"
• Passive builders (tweakUI) options only show when playing + auto scales according to resolution


9.19 → 9.21
27/11/2015

• Added widget: "Darken Map": default enabled, ctrl+alt+[ or ], remembers per map, reset with /resetmapdarkness
• Bloom Shader: intenser + darkens map a bit
• Bet Frontend: added GUI to do a bet + 'select bet units' button
• Ally Selected Units: when tracking player: displays checkbox to opt out following their selection
• Ally Resources: got smaller for lower resolution screens
• EnemySpotter: bugfix for when shaders were disabled


9.18 → 9.19
21/11/2015

Balance changes:
• Core Underwater Moho Mine cost 10% less metal
• "Advanced Construction Sub" metal cost reduced by 20%
• "Seaplane Platform" metal cost reduced by 20%
• Pincer (ARM Light Amphibious Tank) • harder to EMP + moves faster
• Garpike (CORE Light Amphibious Tank) • harder to EMP + moves faster
• Cloakable Fusion Reactor produces 50 more energy

Others:
• Advplayerlist: doubleclick playername: will mirror the player's selection too!
• Ally selected units: shows for spectators too.
• GUIshader: slightly intenser blur
• redUI Minimap fix: fixes engine minimap being larger than redUI-minimap background/buttons container


9.16 → 9.18
15/11/2015

• fixed "Ally selected units" error spam


9.15 → 9.16
15/11/2015

Others:
• Ally selected units has ben transformed into gadget
• ecostats: dead teams no longer show + has a fixed relative position (prevents it from moving down a bit after an ffa)
• advplayerlist shows who has betted and what score they have
• bet frontend enabled by default + added command: /selectbets
• bugfix glitchy water for "map edge extension" widget
• redui minimap: added a border
• small perf increase for various widgets


9.14 → 9.15
07/11/2015

Balance changes:
• It's easier to paralyze bantha (paralyze multiplier = 1.3)

Others:
• bugfix transports causing invisible units
• bugfix for the bet system


9.13 → 9.14
06/11/2015

Balance changes:
• Air Transport speed will be slowed down when lifting heavy loads.
• Fixed unloaded units sliding bug
• Fixed units failing to unload + fixed unload through cliffs
• Disabled "dgun charge" because "transporting commander" bugs were fixed

Others:
• Added beta version of "Bet Frontend" (default off) see commands widget for all its commands
• Added "Bloom Shader" widget (default off)
• GUI elements have been given a faint border
• Map-info widget notes map size aswell
• Fixed halos for enemy units
• Renamed "HighlightSelectedUnits widget: added spaces (widget will be enabled again if you had it disabled)


9.12 → 9.13
30/10/2015

Balance changes:
• Buzzsaw and Vulcan are having "hold fire" by default
• Buildtime increased by 15% for advanced fusions
• T2 Missile ships accelerating a little bit faster
• Adv crawling bomb is moving faster (1.75 → 2.8)
• Pyro have 5% less HP
• Termite metal cost decreased by 10%
• Sea to air torpedo launchers are removed

Others:
• Added "Commands info" widget
• Resurrection halos for enemy units too
• Removed groundplate from the factorries decals + nanos have a decal again
• Added "Pause/Unpause sounds" widget (disabled by default)
• "Shadow Quality Manager" widget has new max quality: 6k (was 8k) and low: 3k (was 2k)
• "LockCamera widget" removed (became obsolete, advplayerlist has it already)
• "commands FX" adjusted appearance slightly (more subtle)
• Removed "Meowl" mascotte
• Removed redUI minimap border


9.11 → 9.12
23/10/2015

Balance changes:
• Increase cost of Annihilator by 10%
• Increase cost of Doomsday Machine by 15%
• Bigger blow radius for air cons (128 → 160)
• Intruder (core t2 vech transport) HP increased (12 500 → 20 000)
• Air transports are harder to EMP
• Cost of T1 and T2 land bombers decreased by 5%
• Dominator's reload time increased (7 → 8) and damage (750 → 800)
• Partially restore old dgun behaviour, now dgun will stick to ground (not water surface)

Others:
• redUI tooltip: added "/unitcounter". See total units on map (note: as player its just your teams total units)
• Advplayerlist: added "/cputext". Shows cpu usage in % instead of the icon
• Added new widget "gui_transport_weight_limit" • when pressing Load command, it highlights units the transport can lift
• Map Edge Extension widget enabled by default


9.10 → 9.11
16/10/2015

Balance changes:
• EMP'd will drain some energy (t1 storage • 60E, t2 storage • 400E)
• EMP'd metal storage will not store + will waste stored metal if you had more then you can hold without emped storage
• Improved "passive builders" gadget: solars will be build even you have no energy
• Enemy unit napping (except commanders) is enabled by default (you can disable in host settings)
• EMP spider regenerates faster (20 → 30)
• Return "old" weapons to T2 missile ships
• T1 metal storage have 10% more HP

Others:
• Atomic bombers are not crashing anymore(to prevent shooting bug)
• Show enemy commander counter by default
• New widgets: "External VR grid" and "Map Edge extension" (disabled by default)
• New widget: "Team stats" button (disabled by default)


9.09 → 9.10
25/09/2015

Balance changes:
• EMP spider regenerates HP
• Commander's capture speed increased 2x (900 → 1800)
• Decoy commander can capture (900)
• Fidos are turned ON by default

Others:
• Pause screen text is more visible
• Widget selector: when clicked outside widgetlist/links: hiding screen
• Advplayerlist mascotte, added: Meowl
• Bugfixes


9.08 → 9.09
18/09/2015

Balance changes:
• Increased range of arm emp spider (220 → 280)
• T2 spiders (Termite, Recluse, Spider) are more EMP resistant
• Removed rockets wobbling for ARM "All-Terrain Rocket Spider"(Recluse) and added 1 more rocket (3 → 4)

Others:
• Added new widget "vignette" (darker at screen edges)
• Added widget "AdvPlayersList mascotte"
• Restyled "widget selector" (F11)
• Increased performance for "anti ranges", "energy conversion" and "red ui drawing" widgets


9.07 → 9.08
11/09/2015

Balance changes:
• Fixed Gimp (t2 amph kbot) sonar visibility

Others:
• ecostats widget: restyled, fixed errors
• some fixes for start boxes, redui etc


9.06 → 9.07
04/09/2015

Balance changes:
• Weakened T1 popups when closed (Increased damage modifier: 0.15 → 0.25)
• Decreased t2 air cons build power: 120 → 100

Others:
• Commanders are not rotating body when assisting lab
• Added new loadscreens
• Fixed pause screen
• Restore engine default los colors when disabling ba_los_colors widget
• Added ecostats widget
• Fixed grey lining at the borders of buildmenu icons


9.05 → 9.06
21/08/2015

Balance changes:
• T1 air constructors: Reduced speed (~12%) and increased build power (~22%)
• T2 air constructors: Reduced speed (~20%) and reduced build power (~30%)

Others:
• Unit info screen now  toggles with CTRL + U (instead of just U)
• Added new loadscreens and removed a some old ones
• Load screen auto fits window/screen size
• Only nano towers are on passive by default. Press Ctrl+F11 to toggle for factories and cons
• Fixed rare error in energy converters gadget
• Corrected descriptions of energy converters


9.04 → 9.05
14/08/2015

Balance changes:
• Energy converters: generate around 16.5% less metal
• HP of t1 vechicles increased by 5% (except scout, cons, minelayer)
• All air now collide (except scouts, sonars and fighters)
• T1 bombers are 3% slower
• T2 bombers are 8% slower but energy cost was decreased by 10%
• T1 artillery now cost 10% less metal

Others:
• Added widget: "unit info" → select unit and press U, or use /unitinfo armcom
• Highlight unit widget enabled by default + decreased intesity and disabled for features. (possible issues for some ATI users, plz report!)
• Metal output for energy converters is showing in tooltips
• EMP'd energy converters are not producing metal any longer
• Wind display remembers position again
• Resource bars show decimals again for a in/out value lower than 10
• Point tracker: disabled by default, and removed in screen drawing.
• Changed pause screen style a bit, background now becomes fully transparant.
• Resize minimap works again without being in ctrl+f11 mode.


9.03 → 9.04
07/08/2015

Balance changes:
• Area-of-effect for "Dominator • Heavy Rocket Kbot" increased, but edge-effectiveness was decreased a little
• Max paralysis time of mobile units was increased to 20 seconds
• HP was increased for "Spider • All-Terrain EMP Spider"
• Increased metal cost of t1 air scouts

Others:
• Awards: fixed background
• Wrecks are visible out of LOS again


9.02 → 9.03
07/08/2015

• Features outside LOS won't show (except for Gaia ones)
• UI elements are now only movable when in TweakUI mode. (CTRL+F11)
• Allyresbars: use /allyresbars_sizeup and /allyresbars_sizeup to scale. (uses pixel position rounding, size changes can jump up/down suddenly)

Bugfixes:
• rounded corners: fixed small gaps
• Metalmakers work again (reverted EMP 'fix').
• Changelog widget able to load changelog.txt.
• Buildbar now remembers its icon-size. (press F11, hover over it + scroll to change iconsize)
• mapmarks-fx flicking issue
• attack AOE: Dgun path display is corrected with an offset


9.01 → 9.02
03/08/2015

Balance changes:
• Arm Atomic Bomber now kills commander (without EXP) with 1 missle.
• Reduced areaofeffect for Bertha and Intimidator to make them less OP vs units.
• Increased commander sonar distance to match sightdistance.
• Decreased max speed of Valkyrie and Atlas (t1 air transports)
• Enabled 'collide' unit property for: Aircons + Krow, Brawler, Rapier, Valkyrie and Atlas.
• Update game energy conversion gadget (when metalmakers are EMP'd they wont produce metal) 

Others:
• Added "Changelog" widget: you can now browse the changelog.txt ingame!
• Added "EMP + decloack range" widget: displays spy and gremlin EMP and decloack range (when selected).
• Build ETA: a bit offsetted to the bottom, so its better readable when in overhead camera.
• Buildbar: disables when becomming spectator.
• Smart Select: now enabled by default.  (to not ignore buildings use: /selection_mode)
• Various minor style tweaks.


9.00 → 9.01
28/07/2015

• Added "show orders" widget: SHIFT+SPACE: shows all active orders on the map
• Fixed upsidedown hovertank unitpic + a few unprocessed unitpics.
• BA LOS colors widget: remembers ; mode + fix for non english layouts + color presets + changed LOS commands to /losradar and /loscolor
• Remove "active/passive" commands handling from immobile builder widget (it was moved to "passive builders" widget.
• Added "passive builders" widget. All cons and labs are on passive by default except commanders and commando.
• GUIshader: fixed the occasional visual bugginess.
• RedUI console: removed GUIshader blur, toggle it back with: /consoleblur
• RedUI build/order menu: toggle iconspacing with /iconspace
• RedUI resourcebars decimal values are stripped.
• RedUI removed 1px space gap at screen edges.
• Initial Queue: bugfix: will not remember queues between different games.
• Resurrection halos is now a widget (no more halos for enemy units)
• Enemyspotter: changed default: renderAllTeamsAsSpec to false, + use: /enemyspotter_highlight for a highlight.
• Ally resourcebars became a tiny bit larger again.
• Highlight selected units, cleaner highlight effect.


8.18 → 9.00
24/07/2015

NEW devs/maintainers:  Decay (balance/mechanics)  +  Floris (graphics/UI)

Configurable widgets
• Healthbars got a border around them. (toggle itwith /healthbars_style) wrecks got smaller decolored bar, only shows zoomed in more.
• Ally-cursors now show playernames next to them. (toggle with /allycursorplayername and /allycursorspecname)
• Added snow widget. Addes snow to maps using a snowy name. (toggles with /snow, and remembers setting per map)
• Added Smart Select widget. Selects units as you drag over them. (keys: SHIFT: all, CTRL: invert, Z: same type, SPACE: new idle units)
• LOS colors greyscaled + use ';'  key to toggle between los / los+radar
• LOS view is enabled by default. If you dont like it • just disable widget "LOS View"(gfx_los_view.lua)

Others
• Rezzed units will get a small halo above them.
• Enemyspotter looks better and has increased performance.
• Commands FX, lines are now textures with V shaped arrows + glow at endpoint diminishes over time.
• Added Shadow quality manager: sets shadow quality max at start and lowers as average fps gets lower. (this widget wont enable shadows)
• BuildETA is slightly smaller.
• Units with self-d command show wit ha skull icon and countdown time.
• Units that were given to you will show a 'new' icon. It fades out gradually, unless they are out of sight, then the fadeout process starts over.
• Smooth camera widget is slightly faster in moving camera.
• Projectile lights are less bright now.
• Customformations got a more glowy endpoint texture
• Added highlight selected unit shader widget. Uses health colors. (default not enabled, wont render highlight for cloacked units)
• Added Xray shader widget. Gets more instense when zoomed out. (its based on ZK version, but with improved performance)
• Added anti ranges widget. Fades when zoomed in. Purple: anti being build. Red: building complete, 0 in stock. Orange: 1 in stock. Yellow: more than 2 in stock.
• Commander name tags: different name style. when zoomout stays large.
• Map Startbox: fixed jagged edges + Commander name tags styled names.
• Added mapmarks widget: draws growing circle at newly placed mapmarks. Erasing also shows a little ground-glow feedback.

GUI
• Rounded borders for all backgrounds.
• Uniticons were streched out a lot everywhere, now reduced that to nearly squared.
• All uniticons are re-processed with a small bevel and rounded corners.
• Added GUI shader: blurs background of various GUI elements. (disable widget to remove the blur, change its style with /guishader)
• Red UI completely restyled.
• Red UI build/order menu: only shows paginator when it is required, uses space to draw extra row of icons.
• Red UI fix: not able to move elements. in f5 (hidden gui mode)
• Red UI Energy/metal resource bars got a gradient applied. Also did this for order-menu toggle button 'leds'.
• Selected units bar restyled.
• Volume OSD has half as much bars and is restyled a bit.
• Added wind strength display. Shows average windspeed in bottom right.
• Comcounter: small style adjustment.
• Replaybuttons: restyled
• Added catchup (reconnect) status bar.
• Simplified energy conversion slider. Made slider draggable over the whole display.
• Console displays recent messages a lot longer (30sec). Console shows 6 lines but when pressed ctrl it will show 10.
• Ally resource bars got restyled. Also uses same player-order as the advplayerlist. Auto-scales with resolution.
• Advanced playerlist restyled. Doubleclick for camera tracking. Country flags! See if spectators using camera or move mouse. Improved res-slider bar responsiveness. Click to hide spectators Scale buttons + auto-scales with resolution.
• Added mapinfo at bottom left of the map, displaying mapname, author and description
• Initial queue: same style as new RedUI buildorder menu.
• Restyle keybind info display. The button will slide to the leftside at gamestart.
• Buildbar restyled.

Removed:
• Open Hosts widget
• Lockcamera UI


8.17 → 8.18
16/07/2015

• Updates for Spring 100.0
• Baked unitdefs_post and weapondefs_post into unitdefs
• Added widget(+gadget) to collect unit statistics 
• Added widget to remember the camera mode
• Added widget to enable LOS view (default disabled)
• Added widget to stop self destruct orders with a stop order
• Added warning when using too old/new Spring version
• More death messages
• Fixed lagging players sometimes not being takeable
• Fixed toaster sometimes not being resurrectable
• Fixed anti-nukes shooting at nukes that fly overhead
• Fixed Mavericks fight command at increased range
• Anti-nuke missiles fly faster
• Increased Corvette health 1650 → 1900
• Max paralysis time of mobile units is 15 seconds, except for mobile anti-nukes


8.16 → 8.17
26/04/2015

• Fix typo


8.15 → 8.16
26/04/2015

• Added widget for changing game speed in replays
• Added widget to display blast radius when placing buildings (press meta/space)
• Added widget to swap Y and Z for AZERTY keyboards
• Added allow/disallow user widgets option to widget selector
• Replaced Newbie Help widget with Keybind Info widget
• Joinas results in becoming a spectator
• Fixed com name tags showing name of substituted player


8.14 → 8.15
22/03/2015

• Fix luaui reload from widget selector
• Reduced metal in missile truck wrecks


8.13 → 8.14
21/03/2015

• Fix AdvPlList reporting phantom substitutions
• Missile trucks can fire backwards (removed maxangledif)
• Slightly reduced workertime of Kbot cons


8.12 → 8.13
20/03/2015

• Tweak Mavericks, more range growth, more initial hp, less hp growth 
• In-game ignore also affects players talking from the battleroom
• Show limexp in tooltip instead of exp
• Allow substitution for players who don't place a startpoint
• Players who join midgame are allocated to empty teams


8.11 → 8.12
08/03/2015

• Workaround for engine bug that caused desyncs in replays
• Fixed Com Counter sometimes not showing


8.10 → 8.11
07/03/2015

• Added 'luaui reset' and 'luaui factory reset' commands to Widget Selector
• Use meta (space) to queue set target commands
• Fixed walls being visible to enemies without LOS
• Fixed maverick exp growth
• Mavericks gain range bonus with exp (multiplier 1+exp/10)
• Slightly reduced sniper speed


8.09 → 8.10
15/02/2015

• Ctrl+click on name in AdvPlList toggles ignoreplayer on/off
• Fixed Liche auto-firing 
• Fixed ghosted features


8.08 → 8.09
08/02/2015

• Widget Selector remembers scroll position, has more useful options
• Widget Selector has +/• buttons to increase/decrease size
• Widget Selector puts Widget Profiler at the top
• Stop commands also stop self destruction
• LuaUI recieves FeatureCreated/FeatureDestroyed callins for all features
• Liche does not drop target after firing 


8.07 → 8.08
31/01/2015

• Nicer GUI for Widget Profiler
• Fixed Help not hiding when widget was removed
• Fixed Substitutions
• Fixed Built Split and Easy Facing not working together; Use the middle mouse button while queueing to activate Easy Facing
• Added State Remover widget, removes return fire and roam states (default disabled)


8.06 → 8.07
18/01/2015

• Fixed spiders slipping while climbing steep cliffs
• Fixed start screen being non-random
• Fixed startpos sometimes being after reconnect
• Fixed carriers drifting when landed on
• Added Commands FX widget (thanks Floris!)
• Added "help" tab to display Newbie Info ingame
• Added Factory Hold Position widget (default disabled)
• Added Widget Profiler
• Ready button flashes
• Slightly increased Sokolov range, removed MaxAngleDif
• Lowered damage reduction of T3 Hovertanks Vs land
• Commando doesn't build crawling bombs, slightly reduced build range
• Changed units built by engineers: Freaker builds (Commando, Pyro, Gimp), Consul builds (Rocket Spider, Fido, Maverick)
• Made Gimp sonar stealthy, increased dps of torpedos
• Reduced cost and buildtime of Seaplane Platforms
• Reduced Zeus health


8.05 → 8.06
21/10/2014

• Fixed passive builders lua error
• Spies have sonar stealth
• Fixed Set Target on ally units
• Improved hotfix for stuck in draw mode


8.04 → 8.05
20/10/2014

• Improved performance of Passive Builders gadget
• Passive builders don't show as resource pull unless they are using resources
• Added numpad keys for camera control
• Added q key for drawing


8.03 → 8.04
16/10/2014

• Removed no longer used DGun Limit modes
• Fixed Red Console not catching spammed "wrong version" connect messages
• Fixed UW Gantry not being buildable in deep water
• Fixed Sokolov and Lun missing sonar
• Cleaned up modoptions


8.02 → 8.03
11/10/2014

• Comblast/Dgun range always shows for selected coms and enemy coms
• Fixed Ignore List
• Fixed Set Target errors
• Added "o" to rotate buildings (hopefully _everyone_ has an o key...)
• Hotfix that should prevent most of getting stuck in draw mode


8.01 → 8.02
09/10/2014

• Fixed mapmark names after substitituion
• Fixed cancel target command
• Added "Alternate Chat Keys" widget, with old style keys, default off
• Added , and . keys to rotate buildings (hopefully works on all keyboards)
• Hotfixes for f6 and backspace keys
• Removed lightning sound


8.00 → 8.01
08/10/2014

• Updates for Spring 98.0
• Players who drop before the game starts can be substituted by specs (provided the TS difference is small enough)
• Added Open Hosts widget to display a list of currently active hosts to specs
• Added (unsynced) commands /ignoreplayer <name>, /unignoreplayer <name>, /ignorelist 
• Ignored player list is remembered between games
• Added a meteor shower to Armageddon
• Added a new Limit DGun mode "charge"; if set, firing DGun uses/needs 10% charge, charge replenishes by 1%/s, is set to 0% on unload
• Added a startpoint guessing routine for continuous metal maps
• Added FFA startpoints for Throne, Dworld, Mearth and Blindside (see **)
• Added special smoke to Commander explosion for top ranked players
• Added queue functionality to Set Target
• Comblast/Dgun range only shows when an enemy unit is nearby
• Passive Builders behave more intelligently
• Improved scoring for efficiency award: (dmg dealt)/(cost of units)
• Default line command is always move
• Fixed Lock Camera interaction with SpecFullView
• Fixed commandos sometimes sliding across the map on unload
• Fixed minelayers attacking things that weren't mines
• Engineers don't build Viper/Pitbull
• Slightly increased Rocko/Storm costs and buildtime

• T2 Sea Revamp:
 -Seaplane Platform is slightly cheaper
 -Seaplane Con is more expensive, has more health and workertime, doesn't build U/W Fusion or Moho Metal Maker
 -Seaplane Torpedo Bombers are now Torpedo Gunships
 -Seaplane Bombers/Gunships are more like (normal air) T2 Bombers/Gunships
 -Core Seaplane Bomber drops "dambuster" bouncing bombs, Arm drops "normal" firebombs
 -Arm Seaplane Gunship fires lightning, Core fires plasma
 -T2 Torp Launchers removed → converted to Anti-Air Torpedos, buildable only by T1 Sea Cons
 -T2 Sea Labs are slighty cheaper, T2 Sub Cons are more expensive
 -T2 Missile Ships are very long range/very slow reload (Core paralyses, Arm damages)
 -T2 Sea Fusion and Metal Makers are more expensive
 -T2 Sea Metal Makers float, have same conversion ratio as land T2 MMs
 -Added a T3 hovercraft, "Sokolov" for Core, "Lun" for Arm
 -Added T2/3 amphibious gantry, buildable by Sub Con, builds T2/3 amphibious units
 -Fixed Depthcharges and Torpedo (from Bombers/Gunships) not making a splash
 -Fixed UW fusions displaying health to enemies


7.99 → 8.00
10/06/2014

• Players who drop before 5 minutes in FFA mode won't leave wrecks (increased from 2 minutes)
• Units cannot be closed/opened while emp'ed
• Disabled FPS mode
• Fixed game ending in "never end" mode
• Fixed build ETAs showing with GUI disabled
• Fixed comblast/dgun range circles showing through hills
• Limit DGun lines fade out as camera zooms out
• LUPS won't render for units that are drawn as icons or too far away 


7.98 → 7.99
03/05/2014

• Added widget that Sets Target for each attack command (default off)
• Reduced debris damage 
• Replaced Prevent Draw modoption with Prevent Combomb mod option (default off)
• Dead ally teams start points/boxes are removed from Limit Dgun list
• Fixed FFA mode not removing afk players
• Fixed ready button sometimes reappearing
• Fixed Attack/Move notifications showing for specs 
• Fixed mobile Anti-Nukes not reaching the edge of their range
• Reduced Bantha selfd & death explosions
• Reduced Tac Nuke range 


7.96 → 7.98
15/04/2014

• Fixed ready button showing for spectators


7.95 → 7.96
15/04/2014

• Integrated ready states into Adv Pl List
• Fixed Custom Formations not reverting to default command after line command
• Fixed mobile antinukes trying to attack 


7.94 → 7.95
07/04/2014

• Added new FFA startpoint mode (see [2246])
• Different death messages for teams/allyteams
• Added basic keybind info to Newbie Placer message
• Cleaned up mouse drag commands in Custom Formations:
   → To give a line command: select command, right click & drag
   → To give a area command: select command, left click and drag
   → To area attack (bombers etc only): press a, press alt, left click and drag
• Fixed Arm Medium Mine not exploding
• Fixed Anti-nuke not reaching the edge of their range
• Reduced Leveller damage per shot
• Reduced EMP launcher stockpiletime (65s) and paralysertime (35s), slightly increased area of effect
• Increased freaker death explosion, reduced workertime and handling
• Anti-air will preferentially not target Fink and Peeper 


7.93 → 7.94
16/03/2014

• Fixed T2 radar plane acceleration
• Fixed Com Counter markers
• Fixed DGun Limiter not changing colour for specs
• Fixed sometimes getting two Death Messages 


7.92 → 7.93
15/03/2014

• Fixed lua error in Prevent Share Self D


7.91 → 7.92
15/03/2014


• Added new mode to Limit DGun; when enabled DGun won't fire within radius 450 of an enemy startpos
• Removed defunct Game End modes, simplified modoptions 
• AdvPlList remembers colour of resigned players
• Lock Camera sorts its list to match AdvPlList
• Added more death messages
• Added mod option for Com Counter to count enemy coms, default off
• Fixed Com Counter miscounting
• Fixed aircraft always crashing on death
• Fixed FFA mode not recognizing when a team has resigned
• Fixed Red Console using wrong colour after line break
• Fixed non-amphib land units moving too slowly in shallow water
• Reduced Zeus target move error 
• Increased T2 Bomber E costs and buildtimes
• Increased Sniper costs and buildtime
• EMP Spiders are stealthy, increased health
• Lots of internal tidying up


7.90 → 7.91
12/01/2014
• Improved initial queue detection in Idle Players 
• Made Newbie Placer work with Coop Mode
• Added basic 'how to play' info into Newbie Placer
• Initial Queue switches whole queue on faction change
• Fixed AdvPlList faction change display before gamestart
• Fixed AI choose-before-game start positions
• Fixed crash caused by lua mem excess
• Fixed mex upgrader nil error 
• Fixed some subs being visible on radar
• Fixed spawn for asteroid maps
• Fixed some heaps being rezzable
• Fixed heap reclaiming
• Fixed transportees in non-air transports showing radar/sonar blips
• Fixed ambusher not closing 
• Warcow is only awarded within the winning team
• T1 artillery is push resistant
• T1 jammers can only be built on flat-ish ground
• Reduced shield power, increased regen speed, removed E drain on repulse
• Increased buildtime of T1 subs, slightly reduced handling
• Minor updates for Spring 96.0


7.89 → 7.90
14/12/2013

• Fixed Initial Queue 
• Increased Buzzsaw/Vulcan buildtime, e per shot
• Spies can reclaim again, when cloaked default action is move
• Hid player/spec quit messages after game over


7.88 → 7.89
13/12/2013

• Removed closed damage mods for core t1/t2 Mex (not Moho Exploiter)
• Remade Eradicator/Chainsaw weapon
• Fixed player 0 not recieving some awards
• Effectiveness award requires greater than average damage dealt
• Made Team Platter less annoying
• Various minor fixes


7.87 → 7.88
10/12/2013

• Fixed error spam from prevent_sliding 
• Ally Cursors doesn't show idle cursors
• Fixed comgate


7.86 → 7.87
08/12/2013

• Fixed Ally Cursors spec colour
• Fixed Commandos mine detonation
• Fixed Depthcharge Launcher firing at land
• Fixed rez progress bars sometimes not showing


7.85 → 7.86
07/12/2013

• (forgot to enable waterline hotfix)


7.84 → 7.85
07/12/2013

• Awards are passed to the replay site
• Tidied up modoptions
• Limit Dgun Range now prevents dgunning within enemy startboxes
• Made Armageddon Mode more fun; only the immobile units explode
• NoCloseSpawns doesn't affect cooped players
• Fixed NoCloseSpawns somtimes preventing ok startpoints
• Added widget to show comblast and Dgun range (default disabled)
• Death messages show in white
• Hid superfluous connection/quit messages in Red Console
• Fixed not being able to toggle specs in AdvPlList
• Hotfix for non-waterweapons trying to shoot underwater in 95.0
• Fixed battlesubs ignoring orders while attacking
• Fixed rez subs often not being hit
• Torpedos won't fire at floating mines
• Increased build time of Commandos mines slightly
• Nanos default to passive


7.83 → 7.84
08/11/2013

• Updates for Spring 95.0 
• Added LUA loadscreen
• Fixed StartPointAssist and enabled
• Added NewbiePlacer as modoption 
• Added support for queueing in Set Target
• Made AdvPlList relative to bottom right corner of screen
• Added TrueSkill column to AdvPlList
• Fixed Mex Upgrader not working after rejoin
• Added more death messages
• Fixed SleepAward name colour
• Fixed battleships having sub icon
• Added shards effect for wreck/heap damage
• Increased delay in Autoquit slightly
• All weapons can target features (including dt/walls)
• Fixed Chainsaw/Eradicator sometimes not firing
• Fixed Kroggy footcrusher weapon
• Reduced hp of Fortification Wall, increased m cost
• Reduced closed & open hp of Doomsday Machine, increased e cost
• Reduced T1 subs speed slightly
• Increased Mercury/Screamer aoe, reduced edgeeffectiveness
• Increased Merl/Diplomat speed, tweaked weapon 


7.82 → 7.83
23/09/2013

• Fixed console crash related to joining game after gamestart
• Death messages moved to gadget
• Added CameraFlip widget (press ctrl+shift+o to flip overhead/smooth cam)


7.81 → 7.82
21/09/2013

• Removed "I sent 0 e/m" messages from AdvPlayerList
• AdvPlList doesn't flash a take button for just tiny e/m amounts
• Added some more loadscreens (thanks Floris!)
• Fixed death messages! (in RedUI only, until 95.0)
• Reduced wind death explosion slightly
• Arm & Core Destroyer velocity reduced, sightdistance reduced 
• Removed metal cost from Screamer/Mercury missiles
• Slasher/Samson handling reduced, won't fire backwards, buildtime and airsightdistance increased
• Fixed Pitbull and Ambusher not being hittable by some weapons
• Fixed awards gadget for spectators/coops 
• Fixed awards gadget error on screen resize
• Fixed Hammer barrel animations
• Fixed torpedos hitting ally stuff
• Fixed torpedo launchers being buildable in too shallow to fire water


7.80 → 7.81
18/08/2013

• Fixed lua error when Pop-up Torpedo Launcher died on sea floor
• Fixed units dying when Pop-up Torps rose
• Hid specs after quit in AdvPlayerList
• Fixed 'normal quits' caused by Awards gadgets
• Fixed awards being given to spectators ;)
• Fixed Ally Cursors showing spec cursors to players
• Disabled Startpoint Assist until Spring 95.0


7.79 → 7.80
18/08/2013

• Fixed specs not being white in Lock Camera and Ally Cursorss
• Fixed not being able to resign when had 0 units left
• Prevent spam of "i took" messages from over-enthusiastic takers & fixed text
• Reduce "i took" to a single line and use rounded numbers 
• Require players to use a few resources before getting the efficiency award
• Fixed some other rare lua errors


7.78 → 7.79
18/08/2013

• Updated game end gadget 
• Added awards gadget
• Fixed Startpoint Assist not catching afk players
• Lock Camera and Ally Cursors become gadgets, net traffic halved
• Afk players are takeable (threshold is afk for 90s or afk at gamestart with no initial queue)
• Take reminders are handled entirely through AdvPlayerList
• Units remember exp when resurrected
• Fixed Waypoint Dragger causing crashes for some mice
• Fixed widget handler passing bad arguments in UnitCreated
• Initial Queue orientates its first building towards the map center
• Unit Moving widget moves units forwards instead of randomly
• Wind Generator death explosion gives 'old' chaining behaviour
• Remade impulse of Leveller & Janus 
• Fixed dynamic collision vols that couldn't be hit by some weapons when closed 
• Fixed Dragons Teeth not getting crushed
• Naval Engineers can't build Croc/Triton and T1 Amphib Constructors 
• Increased Croc buildtime
• Fixed torpedo bomber aiming
• Increased death explosions of T1 Construction Ships and Tidal Generators
• Increased T1 Ship Cons builtime and reduced manouevability
• Increased T1 Torpedo Launcher buildtime


7.76 → 7.78
27/06/2013

• Dots in Customformations are of consistent size depending on zoom and terrain height 
• Fixed crash in Customformations when both mouse buttons were pressed at once
• Set Target can now be used with Customformations
• Fixed faction changing in coops
• Workaround for luaui crash on empty BA.lua
• In team com-ends, when game ends, units are destroyed in a wave of death, outwards from last com
• Fixed ambiguities in context build with radar, sonar & dragons eyes.
• AdvPlayerList gives a chat notification when m/e are shared to allies
• T1 Ships Revamp! (see below)
• Added map icon for anti-air & gave scouts a smaller map icon
• Fixed icon size when units are in ground/sea transports
• Fixed Startpoint Guesser sometimes not recognizing genuine startpoints
• Fixed passenger explosions on hover transport death
• Reduced Can maxspeed 1.35→1.25
• Reduced Mercury/Screamer buildcost by about 10%
• Commando only auto-builds mines when movestate is roam
• Added draw/point spam blocker widget (default disabled)
• Made Specific Unit Reclaimer work with all types of constructor


7.76 → 7.77
02/06/2013

T1 Ships Revamp

• Commanders now have an underwater weapon, a short range laser which fires when they are not building/repairing (dps similar to the existing red laser)
• Commanders can now build Floating Radar Towers

• T1 Torpedo launchers built by Commanders and Amphibious vehicles are now initially created on the sea floor and pop-up once when complete.
• Arm T1 Torpedo launcher reload time reduced (1.9→1.7), AoE increased a little (16→48 with 40% edgeeffectiveness)
• Core T1 Torpedo launcher reload time reduced (1.9→1.7), AoE increased a little (16→48 with 40% edgeeffectiveness)
• Both T1 Torpedo launcher turret turn speeds increased a little
• Both t1 Torpedo launchers have flighttime (1.35)

• Arm T1 Shipyard metalcost reduced (615→425), health increased (2990→3700), workertime increased (100→220), energymake added (+15)
• Core T1 Shipyard metalcost reduced (600→415), health increased (2990→3850), workertime increased (100→220), energymake added (+15)

• Arm Tidal Generator energycost reduced (412→288), health increased (256→358)
• Core Tidal Generator energycost reduced (417→292), health increased (253→354)

• Both T1 Floating metal makers energy build cost reduced 10%

• Core Amphibious lab metalcost increased (917→1192)
• Arm Amphibious lab metalcost increased (860→1118)

• Arm Floating HLT Energy Per Shot reduced (75→40), Reload time reduced (1→0.9), Target move error reduced (0.2→0.1), Special damage vs Commanders added (210→300)
• Core Floating HLT Energy Per Shot reduced (75→45), damage increased (210→231), Target move error reduced (0.2→0.1) Special damage vs Commanders added (210→250) 
• Both Floating HLT Turret turn speeds increased a little
• Both Floating HTLs Energymake added (+5)
• Both Floating HLTs Buildtime reduced 5%

• Arm T1 Floating Anti-air Tower Metalcost increased (71→85), Health increased (252→340)
• Arm T1 Floating Anti-air Tower Weapon reload time reduced (1.7→1.2), damage increased (113→125)

• Core T1 Floaring Anti-air Tower Metalcost increased (72→86), Health increased (290→355)
• Core T1 Floating Anti-air Tower Weapon reload time reduced (1.7→1.2), damage increased (113→125)

• Both T2 Ressurection subs moved to T1, costs reduced a little, movement enhanced (Ressurection Workertime 450, Repair Workertime 250)

• Both T1 Construction ships Repair Workertime reduced (250→125), Build Workertime still 250.
• Both T1 Construction ships acceleration increased.

• Both T1 Construction ships added Dragons Teeth & Pop Up turrets (Arm Claw for Arm, Dragons Maw for Core) for anti-swarm coastal defense
• Arm Dragons Claw & Core Dragons Maw maxslope increased (10→18)

• Core T1 Scoutboat footprint reduced, renamed 'Patrol Boat', health increased (228→345), autoheal added (1.5)
• Core T1 Scoutboat laser redone, range increased (220→260), more rapid fire, about 40% more total dps

• Arm T1 Scoutboat footprint reduced, renamed 'Patrol Boat', health increased (224→345), autoheal added (1.5)
• Arm T1 Scoutboat laser redone, range increased (220→260), more rapid fire, about 40% more total dps

• Core Corvette metalcost reduced (367→294), energycost increased (1912→2294), energymake added (+3)
• Core Corvette weapons tweaked, energypershot reduced (20→5) & now do more damage at max range

• Arm Corvette metalcost reduced (378→302), energycost increased (2055→2466)
• Arm Corvette lasers replaced with EMG cannons, no energy cost, roughly the same dps.
• Corvette corpses health reduced, can now become heaps, metal reduced in line with unit metal cost reduction

• Arm Destroyer health increased (2575→3090), sight distance increased (490→550)
• Arm Destroyer Turret Gun reload time reduced (1.4→1.2), damage increased (160→175)
• Arm Destroyer Depth Charge tweaked (fires a little faster, lower damage, more AOE, less move accuracy)

• Core Destroyer health increased (2800→3360), sight distance increased (465→550)
• Core Destroyer Turret Gun damage increased (310→385)
• Core Destroyer Depth Charge AOE increased

• Arm T1 Sub handling improved, small autoheal added, sight distance increased, corpse metal reduced.
• Arm T1 Sub weapon AoE Increased a little, damage increased a little (600→650), accuracy improved

• Core T1 Sub handling improved, small autoheal added, sight distance increased, corpse metal reduced.
• Core T1 Sub weapon AoE Increased a little, damage increased a little (600→650), accuracy improved

• Arm Sea Transport metal cost reduced (919→735), energy cost increased (4639→6239), buildtime reduced (14538→10176)
• Arm Sea Transport small autoheal added (+5), sightdistance increased
• Core Sea Transport metal cost reduced (887→710), eenrgy cost increased (4768→6286), buildtime reduced (13663→9564)
• Core Sea Transport small autoheal added (+5), sightdistance increased

• Both Transport ships can now load and unload units again (workaround for an engine bug)
• Both Transport ships operate in any water depth

• Arm Advanced Shipyard Health Increased (4512→5415), energymake added (+25)
• Core Advanced Shipyard health increased (4416→5300), energymake added (+25)


7.75 → 7.76
19/05/2013

-Try to intelligently choose startpos for players/AIs who didn't place themselves
-Nicer visuals for CustomFormations2 (thanks PixelOfDeath!)
-Added "Set Target" command: 'Sets a top priority attack target, to be used if within range (not removed by move commands)' with keybind to y, cancel target bind to j
-Made AdvPlayerList more compact 
-Fixed incorrect faction showing in AdvPlayerList after choosing faction in-game
-Fixed lua error on com explosion
-AdvUnitMarker now only marks nukes/antinukes/tacnuke/empsilos/buzz/vulc
-Specific unit reclaimer won't act unless alt is pressed 
-Maverick learns exp a bit quicker than other units
-Commando becomes amphib, build range increased →310, health increased →1400
-Mercury/Screamer gets its uber long range back, can stockpile up to 5 missiles
-Fixed gimp not firing in shallow water
-Croc e cost increased →8500
-Juno missile leaves behind 30 seconds area denial for ground scouts within 450 radius
-Transport helper ai won't try to transport scouts


7.74 → 7.75
26/03/2013

-New version to overcome a conflict between rapid and Springfiles versions


7.73 → 7.74
26/03/2013
-Fixed lua errors and odd behaviour caused by change to UnitPreDamaged arguments (fixes combomb, commando and other gadgetry)
-Fixed comgate
-Fixed dgun not firing if there was uneven ground in the way
-Fixed some lua errors and set com_counter to not place markers by default
-Made a modoption for no_close_spawn
-Made adv_unit_marker place only local markers
-Made enemy_spotter widget more visible
-Made menu of lock_camera easier to read
-Made snd_volume_osd enabled by default and made it go pop!
-Removed dynamic_blob_shadows widget 


7.72 → 7.73
23/03/2013

-New loadscreens 
-Added cmd_keep_target widget 
-Added lock_camera widget 
-Added com_counter widget
-Added blackened crosshair cursor to show when an attack command will fail 
-Added collision volumes for almost all units 
-Replaced unit_marker widget with Adv_Unit_Marker 
-Replaced snd_volume widget with snd_volume_osd (→ use -/+ keys to change volume ingame)
-Made enemy_spotter widget look much nicer and handle multiple enemies 
-Made z,x,c,v 'keybinds' work with initial_queue widget
-Fixed t1 veh/sea cons lacking buildrange for t2 labs
-Fixed bad maxwaterdepth making some sea unit unbuildable in 92.0+
-Fixed un-killable paralysed aircraft 
-Fixed mines blocking units in 92.0+
-Fixed coop mode
-Fixed liche 
-Several small bugfixes
-Pushing units is now a modoption, default enabled
-Startpoints now cannot be placed within the dgun range of another start point
-Took away radar, sonar and LOS from crashing aircraft
-Units built by engineers changed: Consul now builds Fido,Zeus,Maverick; Freaker now builds Pyro,Can,Commando
-Increased Panther energy cost 4200→6000
-Removed 50% EMP damage reduction recieved by Bantha
-Vanguard health decreased 12k→9k, reload time increased 6→8
-Mercury & Screamer changed substantially, hopefully they are good anti-air-swarm defence now
-Vulcan & Buzzsaw will now fire at/over/into hills


7.71 → 7.72
21/09/2012

-Fixed Customformations bomb line
-Fixed nuke not firing if order given before missile is ready
-Fixed subs and subkillers firing in any direction
-Fixed nuke bombers refusing to fire at ground
-Fixed aircraft getting stuck on air repair pads
-Fixed reclaiming crashing aircraft giving lots of resources
-Fixed killing crashing aircraft givings -1 XP
-Fixed units getting stuck in labs
-Fixed passive builders not detecting stall condition correctly
-Reclaim command can now be waited
-Added splash sounds
-Crashing aircraft do less damage
-Fixed turninplace for most units, handling and pathing improved
-Added QTPFS modoption
-Amph t1 vec cons now have better acceleration: handling>random nerf
-Added logo (MAKE A BETTER ONE!)
-Auto idle timer changed to 2.5 minutes


7.70 → 7.71
04/09/2012

• Fixed bombers + torp bombers ignoring attack commands 91 (Customformations line attack DOES NOT work for bombers in 91)
• Fixed Transports for 91
• Non gunship aircraft have 50% chance of crashing to ground instead of exploding
• Fixed builddistance for 91 
• Remove blur shader (ugly and resource intensive) 
• Give corsktl a larger hitsphere so unit self explodes correctly 
• Add modified xta Splashgadget with custom cegs 
• Add fixed weaponDefs_post.lua and water hit splash sounds 
• Armsniper weapontype changed to Rifle. Should fix snipers shooting � 
• Torps no longer fire at Pelicans 
• Juno now kills jeffy, flea and weasel. Juno metalpershot cost added, 250M per shot
• Add Kloots dynamic lighting gadget and custom config (more bling) 
• Added dynamic projectile lights widget (bling bling) 
• Reduced all crawling bomb's underwater speed by 33% 
• Further optimized gfx_dynamic_blob_shadow.lua 
• Increased unit under attack warning alarminterval to 15 
• Smoothed out all Kbot animations with smoothanim.py 


7.67(8) → 7.70
25/07/2012

• Perfomance optimized blob shadows (nearly 30% faster) 
• Optimized group label widget 
• Fixed keybind/hotkey screen 
• Fixed cortide yardmap
• Xray widgets removed 
• Guardian and punisher 15% less metal costs 
• Arm cloakable fus cloak cost reduced to 100 (from 200) auto cloaks when built
• Added mute support to red console Syntax: /mute <PlayerName?> /unmute � 
• Merl AOE increased (100→150) Diplomat AOE increased (90→150)
• From BrainDamage: take command for idle players 
• Added 'Prevent Excessive Share' gadget, fixes lost resources on take bug
• Added modoption to switch to classic pathfinder 
• Changed to BrainDamage's dynamic stockpiler 
• Decreased HP of t1 metal storages by 30%
• reduced morty speed by 20% 
• Updated game energy converion gadget, stunned mm no longer produce m, each mm now shows output like old times
• DGUN Unstall widget replaced by DGUN stall assist widget
• Fixed crash in mo_preventdraw when game is acutally a draw 
• Added 3 more widgets on request: cmd_factoryqmanager.lua  gui_idle_builders_new.lua unit_only_fighters_patrol.lua 
• Mex upgrader fix
• Set collisionvolumetest true for all unit's 
• Fixed comm reduced airblast
• Nano towers are now transportable, in t1 transports too. 
• Fix units receiving damage on not-so-nice unloads from transports. 
• Vanguard nerf: hp 15k→12k, weaponvelocity 610→500, predicboost 0.75→0.25
• Plenty of widget and gadget fixes, optimizations for MT.


7.66 → 7.67
24/03/2012

• Removed hacky 87 gadgets
• Added ZXCV building hotkeys
• Added widget enemy spotter which marks enemy units. disabled by default 
• Blob shadow fix


7.65 → 7.66
15/03/2012

• Fixed area reclaim
• Fixed cons getting stuck
• Fixed mexupgrader


7.64 → 7.65
15/03/2012

• Units that shouldnt shoot air now dont
• Fixed submerged nanoframe targetting
• Core adv torp now officially underwater unit
• Area reclaim fixed
• Torp launchers dont target hovers at all now
• Sniper and others couldnt be targetted by most units
• Core aircraft plant heights increased


7.63 → 7.64
11/03/2012

-fixes for .87
-Tank and Hover turninplacespeedlimit=unitvelocity/2
-Kbot turninplaceanglelimit=91
-Torpedos and depthcharges no longer target hovers
-Per piece collision volumes fixed (viper being immune to beamlaser bug)
-Carriers no longer assist building
-Nanos get restarted automatically
-Nanos are built with passive mode by default
-Added ranks api gadget
-Radar units now emit radar and los from their actual radar dishes (results in greatly improved t2 radar and LOS)
-Many widget fixes, and performace optimizations


7.62 → 7.63
24/12/2011

-fixes for engine 85.0
-attempt to fix unit velocities
-units die instantly now in shot down air transports
-fixed unit animations


7.61 → 7.62
29/11/2011

-Better handling for most units with turninplace
-Fix t1 destroyer bad handling (by reverting to old behaivour, a combo of �
-Torpedoes no longer hit hovers
-Fix the Dominator hack
-Added ability for maps to override engine start positions. Thanks zwzsg
-Add Updated air release gadget and new airlab fix gadget , and cmd_lstpos �
-Fix problem with armbrtha hitsphere
-Updated Dynamic Collision Volume gadget to support dynamic per piece �
-Update mex snap Widget
-Viper and Pitbull script fix (thanks KingRaptor and Juzza)


7.60 → 7.61
24/11/2011

• Fixed default widgets and added game end gadget.
• Updated dynamic collision volumes
• Sound config fixes
• Fixed tank and hovercraft maneuverability issues (where they would stop on new orders and on turn)


7.50 → 7.60
09/10/2011

• Fixed CORE Dragon Eye having ARM logo on it 
• Units that couldn't previously can now hit a closed packO
• Energy converter now uses correct efficiencies and capacities from BA 7.31
• MetalMakers now open/close depending on whether they're in use again
• Improved and optimized/beautified all construction unit animation scripts
• Fix for coop players starting on the same position
• Fixed bombers commandfire weapon tag for .83 compatibility
• Added new game end condition gadget for .83
• Fixed Core DDM animation, collision volume and optimized model
• Updated dynamic collision volume gadget 
• Added more custom collision volumes

• Added modoption to toggle whether start resources belong to the team or the commander (default: team)
• Teams that die in FFA mode before 2 minutes get killed without leaving wrecks
• Enemy Transporting mod option now defaults to 'Disallow All' (previously All But Commander) 
• Air Comblast Full Damage modoption now defaults to 'false'

• Fixed submarines not being able to hit some t1 ships by expanding hitspheres
• Sea pathing improved by reducing footprint of smaller boats (only minimal unit overlap) and removing turninplace for smaller boats 
• Dragon Eyes can now float on water
• Added amphibious to description of units lacking them
• Arm & Core Cruiser close-range deck lasers damage per shot increased (60→110)

• Arm & Core T1 Missile trucks dps vs air increased 20%
• Arm & Core T1 Missile trucks airsightdistance 800 added

• Arm Maverick accuracy vs moving targets increased
• Arm Fido buildtime reduced 10%, 'On' weapon AOE increased a little
• Arm Zeus weapon now does 50% splash damage to up to 2 nearby units 
• Core Freaker can now build T1 Construction Ships & Destroyers
• Core Commando mine placing script improved
• Core Can HP increased (4350→4850)
• Core Sumo EMP resistance added (0%→50%)

• Arm Consul can now build T1 Construction Ships & Destroyers
• Arm Bulldog weapon damage increased (240→270), turret aim speed increased a little
• Core Reaper weapon damage increased (97→109), turret aim speed increased a little
• Core Diplomat missile damage increased 20%
• Arm Merl missile damage increased 20%

• Arm Banshee special damage vs commanders raised (3→5) (default damage is 9)
• Core Hurricane bomb damage increased (283→337)
• Arm Phoenix bomb damage increased (210→250)
• Arm & Core Advanced construction aircraft workertimes raised (130→170)
• Arm Brawler hp increased (1400→1600)
• Core Rapier hp increased (1150→1400) 
• Core Krow hp reduced (17500→15000)
• Arm Blade hp increased (2675→2700)
• Arm Dragonfly EMP damage per beam raised (15000→22500) 

• Fighter HP reverted to 7.31 levels
• Fighter special lower damage vs gunships removed
• Fighter vs Fighter damage increased
• Fighter airsightdistance increased
• Hawk/Vamp reload times increased
• EnergyMake/EnergyUse & Idle Autoheal removed from fighters 

• Arm Dragons Claw weapon now does ~33% splash damage to up to 2 nearby units
• Core Double llt top laser range increased (435→475), special damage vs commanders reduced (140→100)
• Core Double llt bottom laser range reduced (435→400)
• Core Double llt Energycost increased (1467→1617), sightdistance increased (455→475)
• Fixed missing Active/Passive switch on Minelayers
• Building mines doesn't level terrain beneath them

• Arm Annihilatior weapon max damage increased from 9000 to 12000
• Core Doomsday machine small red laser now in a burst of 2 shots per round

• Core LRPC (Intimidator) range increased (4000→4950) 
• Core LRPC (Intimidator) reload increased ~20%
• Core LRPC (Intimidator) heightboost factor reduced (6)
• Arm LRPC (Bertha) range increased (4000→4650)
• Arm LRPC (Bertha) reload increased ~20%
• Arm LRPC (Bertha) heightboost factor reduced (8)
• Core Buzzsaw metalcost increased
• Core Buzzsaw damage per shot reduced
• Core Buzzsaw death explosion made much larger
• Arm Vulcan metalcost increased
• Arm Vulcan damage per shot reduced
• Arm Vulcan death explosion made much larger
• Arm EMP Silo range increased (4000→4500)

• Increased plasma deflector coverage (400-500)
• Increased plasma deflector max power (7500→12500)
• Decreased plasma deflector charge speed (150→100)
• Added some initial charge to plasma deflector once built (2000)

• Arm & Core Advanced fusion buildtimes raised 40%
• Arm & Core Advanced Kbot labs workertime increased (200→300)
• Arm & Core Advanced Vehicle plants workertime increased (200→300)
• Arm & Core Advanced Shipyards workertime increased (200→400)
• Arm & Core Targeting facilites energy to run cost reduced (150→100)

• Juno energy per shot reduced (16000→12000), new unit effects added

• Arm & Core Stationary Anti-Nukes energycost increased (28000→40000) (was ~60k prior to BA 7.4)
• Arm & Core Stationary Anti-Nukes buildtime increased (28000→60000) (was ~95k prior to BA 7.4)
• Arm & Core (Ground Based) Mobile Anti Nukes costs reduced ~20%
• Arm & Core (Ground Based) Mobile Anti Nukes coverage reduced (2000→1600)
  
• Arm Bantha EMP resistance reduced (100%→50%)
• Arm Maurauder hp raised (4000→4200)
• Arm Razorback hp raised (11500→12000)
• Core Juggernaut laser dps increased
• Core Krogoth kick AE made a bit larger


7.42 → 7.50

• Fixed EMP affecting units that weren't supposed to be
• Fixed 2 crashes related to ATI cards

• Reverted both HLT hitpoints change back to 7.31 levels.
• Arm HLT buildtime raised (9575→12500)
• Core HLT buildtime raised (9622→12650)

• Idle autoheal reverted.
• Antinuke now stockpiles again (build cost reduction remains in place).
• Fighter HP upped from 50→125.
• T2 bombers now line-bomb again but with less saturation (more like an improved t1 bomber)
• T2 bombers no longer drop their bombs ahead of their target, but drop them vertically as they fly over it.
• EMP bomber has been modified to similar rules to the above and reintroduced.
• Arm Blade HP increased (1800→2675), weapon effect changed (bit more burst damage with longer reload).
• Restored cruise altitudes on aircraft.
• Unit kidnap preventing is now a mod option, select ALL, Commanders only or None at your leisure (Default: Commanders Only).
• Core Goliath HP decreased (8200→7000).
• Core Tremor HP increased (2045→2700).
• Arm Gremlin acceleration increased.
• Arm Maverick now aims faster and unholsters guns more swiftly.
• Arm Recluse missile accuracy increased.
• Arm Spider LOS range increased (360-550) • use them as scouts for Recluses
• Core Termite metal/energy costs decreased 10%, weapon now fires faster for less damage (same dps).
• LRPCs now gain a bit less range from height (heightmodboost 20→10)
• Energy converter conversion should now better match 7.31 metal makers
• Packo/Sam reloadtime and damage cut (faster shooting, sameish DPS).

• A few effects improvements (krog heatray, bantha cannons, vulcan shell casings, etc)


7.31 → 7.40
29/05/2011

No real changelog present, but instead: the changes in repository listed below.

    Readded commando after change 144.
    Intimidator and Big Bertha gains more range from heights: �
    Improved Krogoth heatray effect / sound.
    Fixed gadgets which were removed in commit 65 • Torpedo bombers can no �
    Replaced take reminder widget with a far more efficient version. Probably �
    Reimplemented coop mode. Probably works.
    Removed wobble from weapons that shouldn't have it
    Made Catapult spread more even and circular
    Removed 50% damage reduction from pitbull/viper when closed
    Berthas eject shell casing
    Increased size of brawler LUPS effect to make them noticable
    Add lups effect for armbrawl and corape and experimental effect for bladew
    Removed damage entries against removed armor classes Renamed some armor �
    Removed antibomber armorclass, boosted HP on Eradicator/Chainsaw to �
    Moved juno damage handling to a gadget (and removed the radar armorclass)
    Armordef fixes/ship class merge
    Add floating t2 flak's and adv torp launcher's to defensive range widget
    Add missing waterline def , unit is now builable on water
    Add custom collision volumes for ajuno and cjuno
    Reverted [86], stumpy and raider turret turn rate reverted to 90.
    Karganeth model optimized, weaponvelocity reduced by 50%
    Add extra files i missed on chnage [113] Beautified cafus model and �
    Beautified cafus model and removed unused piece 5 > 4
    Removed Commando pending a scripting fix
    Update lups_shockwaves.lua to reflect changes to weapondefname changes
    luarules/gadgets/lups_shockwaves.lua
    Samson 1065→700 HP Slasher 1120→740 HP
    Heavy optimization of t1 scout planes and t1 and t2 fighters
    Updated metalspot finder
    Reduced EMP launcher range to that of berthas (6000→4000)
    Precision bombers now quickly drop 5 bombs (to fix targeting of moving �
    Krogoth can kick small units only in sync with leg movement
    Antinukes no longer stockpile
    Reduced bertha/intimidator range 6200,6600 → 4000
    Made antinuke energycost/buildtime ratios closer to normal T2 ratios
    Hurricane + Phoenix → Precision bombers (Same single-target damage, �
    Lowered plane cruise altitudes
    Fixed napalm effects
    Fixed preventdraw gadget
    Reduced HLT HP 30%
    Removed arm EMP bomber
    Reduced fighter HP to 50
    Faction change UI now middle-mouse draggable
    Fixed division by zero errors in 2 COBs, my fault
    Added helpful widgets to mod
    Implemented widget blacklisting for likely metal maker widgets (Regex: �
    Customized collision volumes Dragon Teeth and common large wrecks �
    Updated various widgets
    Removed energy drain from underwater T1 mexes
    Increased turret turn speed for Stumpys and Raiders 90→145 deg/s
    Beautified and/or optimized several Kbot animations.
    make svn version public avaiable
    Customized lots of collision volumes
    Krog arms are now shotguns
    Added armageddon modoption (After X minutes, every unit is destroyed)
    Removed storage from commanders, added base storage for teams.
    Added ingame faction change. Coop mode removed (potentially temporarily)
    Beautified and/or optimized several Kbot animations.
    Better on/off animation for ARM M Makers (even though it's not used �
    Custom collision volumes for LRPCs, T3 Labs, Moho Geos, ARM Fusion and �
    Integrates chili also added some other essential widgets
    Removed energy drain from T1 mexes.
    Rewrote passive builders, more efficient, more accurate. Also applies to �
    Added mass limits to T1 transports to make fatboy/sumo untransportable
    Fixed out-of-map destoy gadget
    DGun now able to target units (Doesn't aim ahead)
    Normalized idle autoheal. 1%/second after 30 seconds. Moved terraform from �
    Some minor cleanup for a few wrecks
    Sumos can be napped when moving
    Cleaned up lots of models using 3DO Builder's "Clean up model" �
    Moved gunships to vtol armorclass, increased gunship HP +25% to counteract �
    Added 3 second flight times for guided anti-air missiles (higher than the �
    Changed vulcan script so that it will constantly spin when firing
    Increased all unit terraform speed 5x
    Better collision volumes for LLTs, HLTs, Missile Towers, Shields, HLLT, �
    Custom collision volumes for T3 units (except Bantha)
    Better collision volumes for Toaster, Shiva and Sub Pens
    Beautified animation for CORE T1 & T2 ships. Customized collision volumes �
    Made the flamethrower sound a bit more ear friendly
    Made ocean look bluer
    Made commanders untransportable by enemy
    Beautified animation for ARM T2 ships. Customized collision volumes as �
    Fixed starting resources always being 1000 regardless of setting.
    Set smoothanim = false for all non-Kbots, negligible performance �
    Metal Makers replaced by gadget-controlled Energy Converters.
    Some hax for a better dynamic collision volume for Pit Bull and Viper
    Missed the core Commander script, last commit had core A.K. instead.
    Optimized and improved animation of Commanders.
    Optimized PeeWee? 19 → 15 pieces, improved animation (sync with unit �
    bladewing optimization, 5→2 pieces
    Updated Custom Formations 2 to v3.3 (From v3.2)
    Some more optimizations, improved walking animation, now in sync with �
    small speedup for unitMarker widget
    Fixed some targeting bugs and added new dynamic collision volumes to some �
    Make targeting of units behind wrecks and DTs better.
    Part of waterline fix.
    Custom collision volumes for all factories.
    Fixed waterline tag for all ships, subs and some floating �
    Updated LUPS with GFX card detection for NVidia Quadro series.
    Replaced wake particles with nicer ones from CA/ZK
    Optimized all PNG images with OptiPNG for smaller file size, no quality �
    Core vamp optimized 9→4 pieces
    Core AK optimized, 27→12 pieces


7.30 → 7.31
27/03/2011

• Reverted Podger and Spolier stealthyness to allow stealth mine laying.
• Reverted hitsphere gadget removal to fix large hitspheres.
• Tweaked dynamic collision volumes to allow targetting.
• Fixed fido primary weapon range.
• Added anti out-of-map aircraft gadget.


7.20 → 7.30
27/03/2011

• Fixed pathing for Eraser
• Fixed pathing for Bantha
• Fixed pathing for Construction Ship
• Fixed pathing for Fatboy
• Fixed pathing for Jammer
• Fixed pathing for Pincer
• Fixed pathing for Skimmer
• Fixed pathing for Vanguard
• Fixed pathing for Spider
• Fixed pathing for Invader
• Fixed pathing for Construction Ship
• Fixed pathing for Garpike
• Fixed pathing for Roach
• Fixed pathing for Croc
• Fixed pathing for Copperhead
• Fixed pathing for Scrubber
• Fixed pathing for Spectre
• Fixed pathing for Shiva
• Fixed pathing for Banisher

• Fixed range of Fatboy
• Fixed range of Fido
• Fixed range of Luger
• Fixed range of Crusader
• Fixed range of Warlord
• Fixed range of Pillager
• Fixed range of Tremor

• Fixed stealth of Spoiler
• Fixed stealth of Podgy
• Fixed stealth of Dragonfly (Bonus: Passengers become stealthy)

• Fixed air targeting of Banshee
• Fixed air targeting of Luger
• Fixed air targeting of Sharpshooter
• Fixed air targeting of Pillager
• Fixed air targeting of Diplomat

• Fixed depth of all submarines
• Fixed underwater pathing for all submarines
• Fixed sub targeting of underwater buildings
• Fixed ship targeting for subkiller submarines

• Fixed disproportionate comwreck hitsphere
• Fixed disproportionate solar hitspheres
• Fixed T1 defence hitspheres (are now hitboxes)
• Fixed dynamic hitspheres gadget making units unhittable

• Fixed vehicles being unable to exit vehicle labs due to automatic terraforming
• Fixed Dragon's Claw being mobile
• Fixed Marky (radar kbot) armorclass
• Fixed liche impulse on commanders
• Fixed Doomsday script
• Fixed RedUI chat console


7.19 → 7.20
08/01/2011

• Fixed Commanders starting on the edge of the startbox being teleported into the middle.
• Fixed a healthbars bug (negative display).
• Fixed a load of incorrect model footprints which clashed with movedefs and may have caused bad pathing (mainly affected Sea).
• Added dynamic hitsphere gadget for units such as Viper (thanks Deadnight Warrior).
• Fixed some building footprint sizes / yardmaps (thanks Deadnight Warrior).
• Fixed buggy targetting behaviour caused by (engine) BadTargetCategory issue, most noticable on Commander, Slasher, Samson, 
• Added 'Air Comblast Full Damage' modoption (default on), disable to have an airbourne commander make a reduced complosion.
• Updated Mex Upgrader gadget (thanks Deadnight Warrior) + fixed some global lua errors.
• Re-added minimum builddistance of 128.
• FFA Mode now gives anyone who drops after 8 minutes a grace period of 3 minutes to reconnect before destroying their units.
• Labs should now only play their building sounds in LOS to avoid giving away their type.

• Fixed cormex script (thanks bartvbl).
• Arm Metal Makers sphere now spins when its on.
• Arm Dragon's Eye buildtime reduced 50%.
• Core Dragon's Eye buildtime reduced 50%.
• Arm Twilight energy cost reduced 20%.
• Core Exploiter energy cost reduced 20%.

• Arm & Core Construction Ships should now maneuver better.

• Arm Stumpy energycost increased (1746→1921).

• Arm Pack0 cloak cost reduced (20→12).

• Core Punisher targetmoveerror removed from low trajectory mode.
• Arm Guardian targetmoveerror removed from low trajectory mode.

• Tech 1 fighters should no longer chase ground units unless ordered to.

• Removed the 'Fire Delay' option for Screamer, Mercury, Chainsaw, Eradicator.
• Added some automatic targetting code to the above missile towers ('beta').
• Arm Flakker energycost reduced 30%.
• Core Cobra energycost reduced 30%.
• Mobile and Static Flak damage vs fighters doubled. 
• Arm Mercury energycost and buildtime reduced 30%.
• Arm Mercury missile no longer collides with friendly units.
• Core Screamer energycost and buildtime reduced 30%.
• Core Screamer missile no longer collides with friendly units.

• Arm Phoenix bomb damage reduced (250→210).
• Arm Tsunami bombs dropped per run reduced (8→7).
• Core Hurricane bomb damage reduced (337→283).
• Core Maelstrom bombs dropped per run reduced (8→7).
• Core Advanced Construction Aircraft workertime increased (80→120).
• Arm Advanced Construction Aircraft workertime increased (80→120).
• Core Krow flying energy cost removed, cruise altitude raised (60→80).
• Core Krow frontal laser damage increased (170→250).
• Arm Dragonfly weapon paralyzer damage decreased (64000→15000), reload time reduced (10-8).
• Arm Dragonfly weapon paralyzetime reduced (20→15).
• Arm Liche bomb no longer instantly kills commanders with impulse.
• Arm Liche bomb special damage vs commanders raised (1550→2300)

• Core Reaper energycost reduced 15%, buildtime reduced 15%.
• Arm Bulldog energycost reduced 15%.

• Core Advanced Construction Kbot workertime increased (140→180).
• Arm Advanced Construction Kbot workertime increased (140→180).
• Arm Fido energycost and buildtime reduced 10%.
• Arm FARK HP increased (200→300), small autoheal added, repair speed increased (120→150).
• Arm FARK can now build Dragon's Eye, Marky, Eraser.
• Arm Invader velocity increased (2.31→2.8).
• Core Roach velocity increased (2.2→2.7).
• Core Skuttle velocity increased (1.35→1.75).

• Arm Pit Bull cloak cost reduced (20→16)
• Arm Ambusher cloak cost reduced (40→24)
• Core Doomsday Machine given its own red/green lasers, roughly same dps.

• Arm Marauder weapon damage increased (185→215).
• Arm Bantha hand cannon damage increased (336→365).
• Arm Bantha self D explosion AOE increased (960→1280).
• Arm Bantha death explosion AOE increased (432→600), damage increased.
• Arm Vanguard hp reduced (18000→15000).
• Arm Vanguard energycost reduced 20%.
• Core Krogoth head laser AOE increased, dps increased, energy per shot lowered.
• Core Krogoth rockets dps improved, effects improved.
• Core Krogoth hand cannons small impulse added.


7.18 → 7.19
16/09/2010

• Added the hitsphere fix gadget by kloot & Deadnight Warrior, reduces hitsphere sizes which were increased by engine update.
• Added Ambient Occlusion Groundplates to most buildings, thanks to Beherith
• Fixed the ability to disable units in the lobby.

• Core Commando metalcost increased (618→1126).
• Core Commando energycost and buildtime increased 30%.
• Core Commando drop gadget behaviour tweaked.
• Core Commando added Core Roach to buildlist.


7.17 → 7.18
04/09/2010

• Bomber reloadtimes now set on the weapon defs not via a script.
• Fixed a crash bug in commando gadget.
• Fixed Arm Advanced Fusion energy storage.


7.16 → 7.17

• Fixed units not taking damage from dead attackers.


7.15 → 7.16

• Fixed default unit icons.
• Fixed and improved custom icons widget.
• Disabled heatmapping for all units.
• Better fix for reclaiming features with 0 resources.
• Commander Wreck is no longer thrown across the map by a Commander Explosion.

• Removed the fake lolUI launcher and enabled RedUI by default (should not affect users of other UIs who already have this disabled).
• Fixed Ghost Site widget not displaying buildings under construction.
• Updated Custom Formations to version 3.2

• Fixed some model holes and improved animations (thanks Pizzi1), affects:
  • Core Construction Vehicle 
  • Core Advanced Construction Vehicle
  • Core A.K.
  • Arm Peewee
  • Arm Kbot Lab
  • Arm Conqueror
  
• Arm Phoenix reload time increased (5→9).
• Arm Thunder reload time increased (5→9).
• Arm Liche reload time increased (5→9).
• Arm Liche rocket flightime limit added (1.5s).
• Core Hurricane reload time increased (5→9).
• Core Shadow reload time increased (5→9).

• All Flak DPS vs non-gunships increased 20-25%.
• Stationary Flak turrets (inc Naval Flak) accuracy increased somewhat.

• New Core Commando added to Core Advanced Kbot Lab (experimental).
• Arm Infiltrator given minor reclaim ability.
• Core Parasite given minor reclaim ability.

• Core Juggernaut, Energy storage added (350).
• Core Krogoth head laser damage increased (5000→8000).
• Core Krogoth rockets damage increased (360→600).
• Core Krogoth rockets reload time increased (2.75→5).
• Arm Bantha head laser damage increased (2500→4000).
• Arm Vanguard Energy cost increased (54739→82109).
• Arm Vanguard turret turn speed reduced 25%.
• Arm Vanguard Weapon reloadtime increased (4→6), damage increased (900→1100).
• Arm Vanguard Weapon area of effect reduced (256→192).

• Arm Advanced Fusion, Energy Storage reduced (25000→9000).
• Core Advanced Fusion, Energy Storage reduced (25000→9000).
• Arm Moho Geothermal Powerplant (Hazardous), Energy storage increased (2500→12000).
• Core Moho Geothermal Powerplant (Hazardous), Energy storage increased (2500→12000). 
 
• Core Light Laser Tower, Energy storage reduced (100→20).
• Arm Light Laser Tower, Energy storage reduced (100→20).
• Core HLLT, Energy storage reduced (100→60).
• Arm Beamer, Energy storage reduced (100→60).
• Arm Annihilator, Energy storage reduced (2000→1500).


7.14 → 7.15
14/08/2010

• Fixed reclaim bug for negative/zero resource features.
• Start resources and storage now belong to the commander not the team.
• Fixed coop mode not spawning units for non coop players.
• Moved start resources into mod options.


7.12 → 7.14

• Added fix for new Spring release not spawning units.
• Added fix for new Spring release removal of AllowUnsafeChanges function.

• Added some fixes for MT build lua errors.
• Removed default off widgets
  • FPS Manager
  • Blob Shadows


7.11 → 7.12

• Added more new load screens.

• Modified the brick texture on arm buildings to look less like 20th century house bricks.

• Fixed Core SAM script issue.

• Fixed Ghostsite widget, now does not redraw all ghosted buildings.
• Fixed RedUI console bugs.
• Fixed Ally Resource Bars widget in spectator mode showing the wrong teams.
• LUPS should no longer draw effects on fusions under construction.
• LUPS shockwave effect now used a bit less.
• Turning off Lups Manager widget now also turns off the Shockwaves and Napalm Jitter gadget effects.
• FFA mode will now remove commanders from players who drop in the first minute with no comwreck.
• Healthbars widget now disables the engine ressurect bars.
• Healthbars widget modified the EMP effect.

• Improved Arm bomber effects.
• Fixed Arm and Core seaplane bomber effects.
• Arm Thunder bomb damage increased approx 10%.
• Core Shadow bomb damage increased approx 10%.
• T1 air transports may now release damaged units when destroyed provided they're close to the ground (mid-unload only).

• Arm FatBoy weapon given minor impulse effect.

• Arm Bulldog should not try to target air units anymore.
• Core Reaper should not try to target air units anymore.

• Arm Vanguard Range decreased 100, heightboostfactor increased (bonus range from high ground to low ground).
• Core Karganeth shoulder/head weapon activated, a weak slow loading AA only version of their main missile (mainly for looks).


7.1 → 7.11

• Replaced loadscreens with JAZCASH's higher resolution offerings.
• Added EngineOptions.lua.

• Fixed some UI stuff auto starting when it shouldn't have.
• Added Ally Resource Bars widget (default off).
• Fixed missing minimap buttons on RedUI.
• Fixed Coop Info widget staying on if you did /luaui reload after gamestart.

• Core Avenger fixed the bad airSightDistance tag (now actually 550).

• Arm Guardian High Trajectory impulse reduced a little.
• Arm Guardian Low Trajectory given a small impulse effect.
• Arm Ambusher Low Trajectory given a small impulse effect.

• Core Punisher High Trajectory impulse reduced a little.
• Core Punisher Low Trajectory given a small impulse effect.
• Core Toaster Low Trajectory given a small impulse effect.

• Swapped Mercury and Screamer weapons (Arm had the Core smoke trail and vice versa!).


7.04 → 7.1

• Removed some infolog spam.
• Replaced modinfo.tdf with a shiny new modinfo.lua.
• Added some minor randomisation to a few sounds via sounds.lua.
• Fixed dgun and bladewing shot sound clipping issues.

• Updated X-Ray hilight widget to work with black teams (thanks bartvbl).
• Updated Custom Formations widget.
• Updated LUPS.
• Added Niobium's Loop Select widget.
• Added Niobium's Build Split Widget.
• Replaced LolUI with RedUI (default on for anyone previously using LolUI).

• Added 'Progressive Mining' game mode (default off), all mines start at 25% efficiency and raise to 125% over a few minutes, death resets this.

• Improved Core Fusion lups effect.
• Improved a few effects with the lups napalm gadget.

• Applied patch with small fixes & improvements to a few models (thanks Pizzi1), affects:
  • Core Tremor + Corpse
  • Core Toaster
  • Core Punisher + Corpse
  • Core Floating HLT
  • Core A.K.
  • Arm Vulcan Corpse
  • Arm Vanguard + Corpse
  • Arm LLT
  • Arm Guardian + Corpse

• Core Silencer launch platform is now in a correct position (thanks bartvbl)
• Arm Ranger launching holes do not "jump up" anymore when the missile bay doors are closing (thanks bartvbl)
• Arm Banisher now aims correctly (thanks bartvbl).

• Removed impactonly from a load of weapons, should fix issues with hitting shipyards that are building stuff.

• Arm Dragon's Claw HP increased (900→1200).
• Arm Guardian High Trajectory damage increased 20%, Low Trajectory reload time decreased 10%.
• Core Punisher High Trajectory damage increased 20%, Low Trajectory reload time decreased 10%.

• Arm Panther Energycost reduced 40%, buildTime reduced 20%.
• Arm Gremlin Reload time reduced 25%, damage reduced 25% (same DPS).
• Arm Phalanx Buildtime reduced 25%, Health increased (1510→2350), velocity increased 20%.
• Arm Phalanx airSightDistance tag added (900).
• Arm Bulldog Velocity increased 20%, turnrate increased (378→415).
• Core Croc Energycost reduced 40%, buildTime reduced 20%.
• Core Croc Velocity increased 15%.
• Core Reaper Velocity increased 15%.
• Core Copperhead Buildtime reduced 20%, Health increased (1595→2425), velocity increased 25%
• Core Copperhead airSightDistance tag added (900).
• Core Goliath Velocity increased 5%, Health increased (7000→8200).

• Arm Jethro airSightDistance tag added (800).

• Core Manticore airSightDistance tag added (925).

• Arm Archangel airSightDistance tag added (925).
• Arm Advanced Construction Kbot Energycost increased 25%.

• Core Crasher airSightDistance tag added (800).
• Core Gimp turret turnrate increased slightly in water, doubled on land.
• Core Advanced Construction Kbot Energycost increased 25%.

• Arm Bantha airSightDistance tag added (1100).

• Arm Brawler Health increased 10%.
• Arm Hawk airSightDistance tag added (600), sightDistance reduced (560→300).
• Arm Blade accuracy increased.
• Arm Freedom Fighter airSightDistance tag added (550), sightDistance reduced (530→275).
• Arm t1 Construction Aircraft added buildoption 'Arm Air Repair Pad'.
• Core Rapier Buildtime and Energycost reduced 10%.
• Core Vamp airSightDistance tag added (600), sightDistance reduced (550→300).
• Core Avenger airSightDistance tag added (550), sightDistance reduced (500→275).
• Core Bladewing useSmoothMesh=0 tag added.
• Core Bladewing weapon values tweaked slightly to hopefully improve targetting.
• Core t1 Construction Aircraft added buildoption 'Core Air Repair Pad'.

• Arm Air Repair Pad costs and buildtime reduced.
• Core Air Repair Pad costs and buildtime reduced.

• Arm Defender airSightDistance tag added (700).
• Arm Pack0 airSightDistance tag added (700), sightDistance reduced (520→375).
• Arm Chainsaw airSightDistance tag added (1000), sightDistance reduced (700→350).
• Arm screamer airSightDistance tag added (1200), sightDistance reduced (700→350).
• Arm screamer AOE increased (240-300), edgeeffectiveness reduced (0.25→0).
• Core Pulverizer airSightDistance tag added (700).
• Core SAM airSightDistance tag added (700), sightDistance reduced (520→375).
• Core Eradicator airSightDistance tag added (1000), sightDistance reduced (700→350).
• Core Mercury airSightDistance tag added (1200), sightDistance reduced (700→350).
• Core Mercuty AOE increased (240-300), edgeeffectiveness reduced (0.25→0).

• Arm Archer airSightDistance tag added (900), radar removed.
• Arm Skeeter airSightDistance tag added (800).
• Arm Swatter airSightDistance tag added (800).
• Arm Flakker NS airSightDistance tag added (800).
• Arm Flakker airSightDistance tag added (800).
• Arm Sentry airSightDistance tag added (750).
• Core Shredder airSightDistance tag added (900), radar removed.
• Core Slinger airSightDistance tag added (800).
• Core Cobra • NS airSightDistance tag added (800).
• Core Cobra airSightDistance tag added (800).
• Core Stinger airSightDistance tag added (750).
• Core Searcher airSightDistance tag added (800).


7.03 → 7.04

• Core Exploiter metal extraction fixed.
• Updated Pause Screen widget.


7.02 → 7.03

• Arm Twilight fixed metal extraction, buildtime reduced.
• Core Exploiter buildtime reduced.
• Load hax gadget should ignore loading your own units.
• Reverted solar textures.
• Minor tweak to Core Metal Extractor Script (thanks bartvbl).


7.01 → 7.02

• Fixed an issue with the prevent draw gadget.
• Prevent Draw mode no longer on by default.
• Added a new patch to the load hax gadget.
• Fixed no wrecks mode to use a whitelist for walls rather than a blacklist for wreck names.
• Imported jk's updated otatextures from CA where applicable.

• Added More Sounds widget (default on).
• Rolled back Take Remind widget due to reports of bugs.

• Improved commander laser aim script a little more.

• Juno explosion effect size decreased a bit.
• Core Exploiter metal extraction raised to equal mex, metalcost (188→220).
• Core Moho Exploiter metal extraction raised to equal moho mine.
• Arm Twilight metal extraction raised to equal mex, metalcost (159→190), minCloakDistance (48→66), energyUse(5→3), cloakCost(10→12).

• Core Wolverine AOE increased (88→113).
• Arm Shellshocker AOE increased (80-105).

• Arm Dragon's Claw HP increased (900→1200), closed damage reduction reduced 5%.
• Core Dragon's Maw HP increased (1100→1450), closed damage reduction reduced 5%.

• Arm Banshee buildtime reduced (15%), damage to commanders raised (2→3).

• Added Decoy Commander to amphibious complex.
• Added minor energy generation to Can, Sumo, Juggernaut and Zeus (still all use significantly more to fire their weapons).

• Core Doomsday machine self destruct damage increased (1800→2400).

• Core Karganeth Removed BadTargetCategory=VTOL.
• Core Juggernaut sightdistance increased (720).
• Core Buzzsaw and Arm Vulcan turret rotation speed increased.


7.00 → 7.01

• Fixed enemy dragons teeth showing up outside LOS.
• Fixed some missing sounds.
• Fixed warning and point sounds being played non-globally.

• Added mod option "Commander Ends No Draw", makes last com alive immune to comblast and disqualifies players who dgun the last com with their last com. (default on)
• Added mod option "Show Enemy Wrecks", disable and you only gain instant LOS on your own wrecks. (default on)
• Added a gadget to reduce damage of torpedos / depthcharges to land units when out of water by 80%.
• Fixed the hack in the reclaim fix gadget.

• Updated Defense Range widget to 6.2.
• Updated Take Reminder widget to 3.2.
• Updated Health Bars widget to latest version (faster).
• Added very_bad_soldier's Pause Screen widget (default on).
• Fixed Ghost Site widget rotation and tracking of buildframes, added tracking for enemy features if needed.
• Fixed vertical text centering on some widgets including LolUI.
• Removed a rare FPS loss issue in waypoint dragger widget.
• Tweaked display of Transporting widget (+default on).

• Improved bantha blaster FX.


6.96 → 7.00

• Added new loadscreens.

• Fixed categories for new spring release.

• Added custom icons widget (default on).
• Added customised Waypoint Dragger widget (default on).
• Added new Share Tracker widget (default on).
• Modified Attack AOE widget, idle performance increased.
• Updated Ghost Site widget to 1.2.
• Updated Defense Range widget to 6.12.
• Updated Take Reminder widget to 3.12.
• Updated Custom Formations widget to 2.2.
• Updated Unit Marker widget to 1.3.
• Removed blast radius widget.
• Removed minimap events widget.

• Added SirMaverick's DroppedStartPos gadget (fixes dropped players starting in enemy start box).
• Fixed FFA Mode to no longer destroy units inside enemy transports.
• Fixed a possible workaround the anti loadhax gadget.
• Tweaked Passive nanos gadget, added the switch to t1 Minelayers.
• Renamed "Greenfields Mode" to "No Metal Extraction".
• Removed broken King of the Hill mode (if Alchemist/anyone wants to fix it in a mutator i'll reintegrate)

• Tweaked some death explosions.
• Added gfx for small yellow laser hits.
• Improved Commander laser aiming script, special damages vs air tweaked.

• Arm Jeffy weapon damage reduced (50→35).
• Core Weasel weapon damage reduced (50→35).
• Arm Flea Reloadtime increased (0.4→0.55), death explosion damage increased slightly (5→8).
• Arm Jethro velocity increased 15%, added maxslope=15 tag for combat engineers.
• Core Crasher velocity increased 15% added maxslope=15 tag for combat engineers.

• Arm Freedom Fighter & Core Avenger buildtime reduced 15%, acceleration increased (2.5).
• Arm Thunder & Core Shadow buildtime reduced 30%. 
• Arm Thunder & Core Shadow Metal & energy cost reduced 5%.
• Arm Thunder & Core Shadow bomb damage reduced, area of effect increased.

• Arm Construction Seaplane & Core Construction Seaplane can now build t2 energy / metal stores.

• Core Viper & Arm Pitbull energy cost increased 50%.
• Core Viper & Arm Pitbull damage and reload increased 25% (same dps, slightly lower ROF).

• Core Pyro flame should no longer show up outside normal LOS for enemies.
• Arm Fatboy sightdistance increased (416→510).
• Arm Fatboy Metal cost reduced (1576→1418).
• Core Termite weapon damage increased 25%.
• Arm Recluse weapon damage increased 25%.
• Core Skuttle Energy cost reduced (27470→24723), Buildtime Reduced (18861→16975).
• Core Voyeur movement class fixed (TANK2→KBOT2).

• Arm Razorback weapon tweaked, dps and aimspeed improved.
• Arm Razorback hitsphere streamlined to reduce blocking in groups.
• Arm Vanguard velocity increased (0.8→1.1).
• Arm Vanguard burnblow removed (broke high traj).


6.95 → 6.96

• Added Prevent Load Hax gadget (does exactly what it says on the tin).
• Patch for ressurect bug, should work in most circumstances.
• Replaced Customformations with Niobium's fixed Customformations2 widget.


6.94 → 6.95

• Fixed a bug in BA Allied Cursors where specs would broadcast a cursor.
• Fixed autoquit widget.
• Fixed shield watch gadget again for new spring.
• Updated Select n Center widget as it seems to be marking the wrong start point on fixed/random games.

• Resized Radar icons to 128x128 to fix an issue with some Nvidia cards.

• Arm Spider sightdistance raised (273→360).
• Core Pyro Acceleration (0.25→0.45) and Speed (2.5→2.75) increased, torso turnrate increased (200→275).
• Core Skuttle move velocity increased (1.15→1.35)
• Arm Pelican AA missile can no longer be force fired at ground.

• Arm Panther lighting weapon no longer targets air.
• Arm Panther AA missile can no longer be force fired at ground.

• Core Double LLT buildtime reduced (6592→5448).
• Arm Beamer buildtime reduced (6493→5324).
• Arm Packo costs all reduced by 20% (energy,metal,buildtime).
• Core SAM costs all reduced by 20% (energy,metal,buildtime).

• Core Bladewing EMP damage vs Commanders cut by 33%.

• Arm & Core Submarines given badtargetcategory HOVER (only attack hovercraft if no better targets).
• Arm & Core Construction Seaplanes can now build naval mines rather than land mines.
• Arm & Core Seaplane platform buildlists reorganised (same as land airplants).
• Arm & Core Ressurection Subs workertime increased (200→450), can no longer assist building.

• Arm Vanguard damage increased (750→900), heightboostfactor added (1.15), sightdistance increased (525→625), accuracy increased.
• Arm Maurauder cannon reload time reduced (0.8→0.7), acceleration increased (0.072→0.22)
• Arm Maurauder gains the panther/pelican light AA missile.
• Arm Maurauder walk script improved, turret turnrate improved a bit (110→140).
• Arm Razorback move velocity increased (2.1→2.3), turnrate increased 25%.
• Arm Razorback dps vs air reduced ~25%.
• Arm Bantha move velocity increased (1.32→1.65), blaster velocity decreased (600→400) (mainly so its more visible).
• Arm Bantha self destruct damage reduced (9500→5500) blast range reduced (1280→960).
• Core Karganeth move velocity increased (1.38→1.5).


6.93 → 6.94

• Coop teams should no longer see enemies start points.
• Improved behaviour of passive nanos in relation to estalling.


6.92 → 6.93

• Removed override LuaUI function (player widgets take priority).
• Removed Reclaim Info Widget (buggy).
• Increased text size on LolUI command buttons (you can modify the size within the element settings under Menu).
• Fixed the shield watch gadget (new spring changed how the shield call worked).
• Fixed the prospector widget.
• Added Reclaim Fix gadget (implements old style reclaim).
• Fixed comcounter widget.
• Coop info widget no longer displayed for spectators.
• Coop teams should now see normal teams start points.
• Changing airplant settings should no longer clear their order queue.
• Added new 'Active/Passive' button for nanoturrets, Passive nano turrets wont build when you're stalling.

• Energy removed from fort walls, manual reclaimTime tag added.


6.91 → 6.92

• Added Coop mode + Mod option to enable.
• Added Alchemist's King of the Hill mode + Mod option to enable.
• Re-added No Wrecks mode.

• Added the new LuaUI code which saves a seperate widget config for BA (will allow you to have a config for each mod, some settings may reset on first load.)

• Added modified allied cursors widget (default on).
• Added Com Counter widget, echos number of remaining Commanders in 'Kill all Commanders' mode (default on).
• Updated LolUI to 9th, custom tweaks to make it work better with other UI's (default on).
• Updated Old BA Layout, now disables LolUI when enabled (default off).
• Updated Defense Range widget (default on), added ghostSite (default on), blastRadius (default on), unit_marker (default off).
• Updated Commander Gate effect so it doesn't break with BA Coop.

• Reverted Thud and Hammer weapon to 6.84 stats (see: http://springrts.com/phpbb/viewtopic.php?f=44&t=18585)
• Advanced Metal and Energy storage HP increased 50%, added to 'ANTIBOMBER' armour class, renamed 'Hardened Energy/Metal Storage'.


6.9 → 6.91

• Fixed a bug that disabled luarules for certain players and caused desyncs.
• Renamed 'BA Layout' widget to 'Old BA Layout' so it isn't initially loaded for previous BA players.
• Updated LolUI (Click Menu > Other Stuff > Reset UI if this does not display correctly).


6.85 → 6.9

• Fixed some bad OTA soundfiles for new spring.

• Added Regret's lolui (default on).
• Added Evil4Zerggin's Prospector widget (default on).
• Added jK's blobshadow widget (default off).
• Added trepan's minimap events widget (default off).
• Replaced Highlight unit widget with new Xray Highlight widget (default on).
• Updated Attack AOE widget updated, added a BA specific fix that makes the D-gun indicator much more accurate.
• Updated Advanced Players List widget.
• Updated Defense Range widget.
• Updated Buildbar widget.
• Updated Commander name tags widget.
• Tweaked FPS Manager widget (now default off).

• Added new Prevent Range Hax gadget (prevents units from overshooting outside of FPS mode).
• Added quantum's No Self-D gadget (stops the self d countdown on a shared unit).
• Added Commander gate modoption/gadget (commanders visually teleport in at gamestart) (default off).

• Several weapon effects improved graphically.

• All weapons with AOE of 16 or less changed to 'impactonly'.

• Added t1 torpedo launchers to the 'no direct control' gadget.
• Modified depthmod tags on amphibs set to 0 (no penalty for being underwater).
• Fixed t1 subs torpedo not reaching max range.
• Land Depthcharge launchers projectiles will now bounce once on land (helps them reach water).
• Scoutboats added to the no self pwn gadget.

• Thud, Hammer predictboost cut a bit (this was added before reload change).
• Core Can hitsphere size reduced.
• Arm and Core Decoy Commander's stats improved, cloak added, mines added to buildlist.
• Arm Marky added to the RADAR armourclass.

• Blades no longer take extra damage from t2 fighters (they now take the same as all gunships).
• Aircraft under construction will no longer be automatically fired upon by AA.
• Raised cruisealt on Valkyrie and Atlas slightly (50→70).


6.84 → 6.85

• Fixed Core Termite weapon sound (should not sound super loud on linux.)
• Fixed Bladewings chasing air units, improved their script & behaviour somewhat.
• Fixed Sea planes getting stuck in limbo in certain conditions.
• Fixed amphibious units speed in and out of water (removed scripts, used depthmod).
• Fixed a character encoding issue that prevented the Core Spectre being loaded.
• Fixed Arm Advanced Radar Tower script imprived (thanks [PiRO]Pizzi1)
• Razorback walk script improved (thanks [PiRO]Pizzi1)
• Mobile AA units should no longer chase ground units.
• Fixed Liche and Krow chasing after aircraft.
• Tech 1 Submarines FPS exploit fixed (manual flighttime added).

• Removed 'no wrecks mode' modoption (Never saw a game where players were happy with it being turned on).
• Added Evil4Zerggin & zwzsg's autoquit widget (exits spring at game end if no mousemove after 10 seconds).

• Arm Rector and Core Necro script & acceleration improvements (faster reaction times).
• Arm Rector and Core Necro autoheal waittime reduced, sight distance increased, buildrange increased slightly.
• Construction kbots build distance raised slightly (90→100).
• Core AK and Arm Peewee number of exploding death shards reduced.
• Core Thud and Arm Hammer mass increased (resistance to impulse).
• Core Thud and Arm Hammer damage and reload time reduced (slight dps increase, faster shots).
• Arm Warrior buildtime reduced by 15%.
• Arm Zeus weapon now costs 35 energy to fire.
• turninplace=0 added to spiders and crawling bombs (experimental).

• Commander energy cost raised significantly (for the purpose of ressurection costs).
• Commander capture speed tripled.
• Terraform (Restore) speed on most builders tripled (thanks Trademark).

• Arm and Core Ressurection Sub's Metalcost and Buildtime reduced by 30%.
• Arm and Core AA Hovercraft DPS increased ~30%.

• Arm Consul now builds Panther and Fatboy in place of Fido and Zeus.
• Jeffy and Wezel no longer do self damage.


6.83 → 6.84

• Exploit Fix: AA Kbots (and many other AA units that used 'BOGUS_MISSILE' for targeting) can no longer manually attack ground.
• Added Trademark's wreckage renames (eg. wrecks will now be called 'Vehicle Plant Wreckage' rather than 'Wreckage').
• Cleaned up the feature file of bad object references so spring doesn't crash when you perform certain operations on FeatureDefs from lua.
• Added my Ally Resourcebars Widget (disabled by default).


6.81 → 6.83

• Missile Delay Gadget now works based on % max weapon reload (in 10% steps).
• Fixed No Owner Mode displaying messages for teams that died naturally.
• Added No metal extraction mod option (to allow you to play greenfields on any map without disabling mex's).
• Added some new reclaim GFX for wrecks.
• Added Google Frog's prevent lab hax gadget (stops unattackable enemy units getting inside your labs).
• Stability tweak to Mex Upgrader gadget to fix a random crash that ruined a game I was in (please report stuff like this with infolog.txt).

• Pointtracker widget modified to only show the arrows on the screen edge and minimap markers (if you like the old functionality download the original widget).
• Center n' Select widget simplified, now also marks your startpoint for you before gamestart on Random/Fixed modes and removes your startpoint at gamestart.
• Start Point Remover widget removed.

• Added missing mex select sound.
• Added Collidefriendly=0 and Avoidfriendly=0 to Nukes and Antinukes to fix failure to fire sometimes.

• Screamer/Mercury removed from ANTIBOMBER armourclass, HP raised 25%.
• Chainsaw/Eradicator Missile Delay option added.
• Chainsaw/Eradicator Bomb Resistance, AOE, Range, Acceleration and Edgeeffectiveness all slightly improved.
• Arm Eradicator damage and reload time descreased (raised ROF, same DPS).
• Defender/Pulverizer flighttime decreased slightly (1.7→1.5).

• Core Shadow build costs adjusted (buildtime (9942→7220), metal (131→154), energy (5691→4837)).
• Arm Thunder build costs adjusted (buildtime (9517→6825), metal (130→153), energy (4496→4271)).
• Core Shadow HP raised very slightly (600→615).
• Core Bladewing nochasecategory and badtargetcategory set to Commanders (since they can't paralyze them).

• Arm Beaver & Core Muskrat velocity & turnrate decreased, energycost and buildtime increased.

• Zipper overall build costs increased a bit (buildtime (3168→3960), energy (3506→4382), metal (161→177)).
• Pyro weapon velocity increased (175→265).

• Arm and Core Shield transparency increased.


6.8 → 6.81
20/01/2009

• Fixed missing sound crash with linux


6.6 → 6.8

• No longer dependant on otacontent or tatextures

• New gadget adds 'Land Mode' and 'Repair Mode' to air plants, aircraft inherit these settings.
• LUPS version updated.
• Self damage at pointblank range stopped with lua for the following units: 
  • Arm Flash
  • Arm Peewee
  • Arm Zipper
  • Core Pyro
  • Core Dragons Maw
• Added New Mod Options:
  • (default off) Remove units with no player (useful for FFA games, not advised in team games)
  • (default off) No sharing to enemies (units and resources) 
  • (default off) No unit wrecks (experimental gameplay if you fancy a change)

• Added Evil4Zerggin's Point Tracker widget.
• Added zwzsg's Auto First Build Facing widget.
• updated FPS Manager to use bumpmapped water when applicable.
• Updated Healthbars widget.
• Added Display DPS widget (disabled by default).
• Added BuildETA widget (disabled by default).
• Added Improved Metal Maked Widget (disabled by default).

• Fixed a number of visible CobError's for new spring release.
• Changed newboom.wav to mono to reduce volume issues.

• Arm Hammer now unpacks its weapon faster.
• Core Thud & Arm Hammer increased accuracy vs moving targets slightly.
• Arm Janus corpse size increased.
• Core Raider HP increased by 60, buildtime reduced slightly (3446→3312).
• Arm Jethro & Core Crasher now Amphibious, added to Ambhibious complex.
• Beamer energy per shot increased 1→6.

• Packo/SAM reloadtime decreased: 15%.
• Eradicator/Chainsaw reloadtime increased: 60%.
• Added flighttime tags to many AA missiles.
• Screamer/Mercury firedelay script fixed (previously only worked once!).

• Construction ship acceleration increased slightly.
• Transport hovercraft radar blob size fixed, arm script fixed.
• Core Poison Arrow turret turns a bit faster.
• Arm & Core Torpedo seaplanes damage raised 20%.
• Core Leviathan & Arm Serpant aiming vs close-up ships improved a bit.

• Core Gimp script fixed (can fire if built underwater), must now aim turret to shoot torpedo.
• Core Gimp reload time increased, accuracy decreased, buildtime increased 25%.
• Core Termite weapon gfx improved, dps increased by around 15%.
• Core Can HP increased (3850→4350).
• Arm Recluse weapon slightly more accurate.
• Arm Zeus no longer able to shoot Air.
• Arm Archangel & Core Manticore now Amphibious, added to Ambhibious complex.

• Arm Annihilator damage raised 5000→9000, Beamtime raised 0.3→1.5.
• Arm Annihilator hp raised 3000→5500.
• Toaster/Ambusher dps increases: High Traj +15%, Low Traj +45%.
• Pitbull/Viper buildtime increased by 25%.

• Juno now hits some mobile jammers it didn't used to hit.
• Plasma Deflectors buildtime and energy cost reduced by 25%.
• Plasma Deflectors charge cost raised (100→600).
• Plasma Deflectors no longer totally immune to lower ROF non-heavy plasma weapons.

• Core Catapult rockets now reach their max range more often.
• Core Shiva walk script fixed.
• Core Shiva given its own weapons, it had the Dominator missile and was unintentionally buffed with Dominator range increase.
• All special damages VS T3 mechs removed (aside from certain emp immunity).
• Arm & Core Experimental Gantry buildtime raised by 25%.
• VULCBUZZ armourclass removed, all special damages vs VULCBUZZ removed.


6.5 → 6.6
14/12/2008

• Raised LosMipLevel and AirLosMipLevel for a great reduction in lag

• Fixed Krogoth vlaunch misfiring
• Fixed Liche autofiring
• Fixed Recluse range
• Fixed some gfx corruption in bomber explosions
• Fixed the 'no more mexs to upgrade' notification on the mex upgrader gadget being sent to every player

• Added moho exploiter fix widget
• Added proximitypriority tags to some high trajectory cannons so they prefer further away units
• Added collidefriendly=0 to some aircraft weapons to stop them hitting eachother when tightly packed
• Added some custom textures to arm and core missile trails
• Added some weapon gfx effect improvements (Zeus, Bantha)
• Upgraded defense range widget
• Fixed take reminder widget (sends the proper /take command now)
• Added the 'no duplicate orders' widget

• Removed an unused 'FORT' category from the SAM
• Removed seismic sig from stumpies
• Reduced the volume of metalmakers on/off sounds

• Beamer turret rotation speed increased, targetmoveerror reduced slightly
• Double LLT tweaked so each laser can find different targets
• Double LLT now slightly more energy efficient than two llts (-60 vs -80 drain on constant fire)
• Dragons claw, Dragons maw no longer attempt to attack aircraft
• Added 'DragonsDisguise' gadget, this can stop units from noticing dragons claws/dragons maws until they've popped up

• Blade speed increased (~5 to 8), renamed from 'Heavy' to 'Rapid Assault'

• Zeus buildtime lowered by ~15%
• Fido speed increased by 15%

• Raised burst DPS on SAM, packo slightly
• Chainsaw & Eradicator now deal good burst damage at range rather than low damage over time.
• Screamer/Mercury now have a fire delay button, you can specify per turret how many seconds to wait before firing once an enemy is spotted (0-5)

• Reduced the chain explode factor on the lighter tech 3 mech deaths
• Kargs and Razorbacks can now target features (ie, can eventually shoot through corpses & dragons teeth)
• Razorbacks acceleration and turret speed increased slightly
• Raised the Arm Vanguard HP (18000)
• Juggernaut main cannons now no longer avoid features (it wouldn't attempt to fire through corpses before)
• Lowered Juggernaut HP (300k)
• Bantha hand cannon dps increased
• Increased buildtime on Bantha, Juggernaut, Krogoth
• Increased workertime on gantries slightly
• Reduced the energypershot on Vulcan & Buzzsaw (constant fire: vulcan -18k, Buzzsaw -21k)
• Bantha is now amphibious


6.41 → 6.5
12/10/2008

Fixed a crashbug with the areaatack gadget.
Fixed LUPS
Fixed Customformation widget


6.4 → 6.41
21/09/2008

Kill All Enemy Commanders, really is the default game mode ;)
Arm Phoenix Script fixed
Fixed CustomFormations widget for 0.77
Fixed MexupgradeGadget


6.31 → 6.4
21/09/2008

Renamed end game modes so its more clear what mode does what
Kill all enemy Commanders is now default end-game option
Added a widget to show which mode is used at the start of a game
Added Widget to display which endmode is active
Fixed firepoints for HLT,HLLT,Pitbull,Flagships,Battleships,Cruisers,Destroyers
Units which are being transported by a Intruder, wont die when a intruder dies.
Fixed yardmap of Core Adv kbot factory.
Mexes can be made it shallow waters now, UwMex mindepth changed to 15 (this change also affects mohomexes)
Nerfed Dragons Claw anti air capability
Removed the non-working anti-air gun of the phoenix
Increased DPS of Warlord, increased laser range a bit too
Increased DPS of the main weapon of the blackhydra
Reduced Arm Saber costs
Increased range of Dominator and Morty
Made zipper EMG, truely look like EMG and increased DPS
Nerfed Scouts/flea anti-air capability
Commando removed
Lowered cruise alt of T2 transports
Increased wezel LOS a bit
Increased storage level of adv. Energystorages
Goliaths no longer target air
Mines/Crawling bombs can now be set on hold fire
Added Adv. Playerlist widget by Marmoth
Added Attack AoE widget by Evil4Zerggin
Updated defense range widget


6.3 → 6.31
29/06/2008

Down graded LUPS to the 6.21 version, to fix the desyncs


6.21 → 6.3
28/06/2008

Flagships have the same movement as other ships now
Core nanoturrets can no longer be build in the water
GIMP torpedo reloadtime increased
Croc and Triton leave a wreck now
ARM and CORE adv. Torp. Launcher have the same minimum depth now
removed the annoying cannot reach destination sound
Added Commander name tags widget, Thanks Evil4Zerggin and CarRepairer.
Added FPS-manager widget, Thanks quantum
Made Crusaders more expensive
Reduced Gunship chain reaction
Fixed the reloading of the Core Catapult
Removed the unused turret of the Arm Razorback.
Added Take remind widget written by Evil4Zerggin
Added Commends and highlight widget written by trepan
Updated quite some widgets, by comparing them to CA versions, Thanks CA Team!!
Added a set of new game-ends rules, in mod options, made by KDR_11k:

 Make sure you put the game on: Game continues if commander dies.
 Then pick one of the mod options:

 •  Kill Everything: Just disables all of the gadgets and lets normal Spring rules apply.

 •  Commander: Team based com ends, if an allyteam has its last com destroyed the whole
	  team is eliminated, as long as one player in the team has a com left the whole team
    remains in play. 

 •  Commander Control: In addition to the above a player without a com is unable to give
 	  orders to his units, all he can do is share them to an ally (sharing to enemies and
	  self-d are disabled). An ally can take his units by using the ".luarules take" command.
	  It was unfortunately not possible to merge this into the regular .take. 


6.2 → 6.21
03/22/2008

Fixed Error messages from the luashockwave gadget?
Fixed Amphid Speeds
Fixed Anti-nuke type
Reduced Seaplane-fighters LoS


6.1 → 6.2
21/03/2008

Fixed directcontrol gadget.
Fixed Layout gadget to not crash on /luaui reload, thanks eriatarka
Reduced Los of fighters to their weapon range, did not do sea planes yet
Added collide=0 to the brawler (forgot it last release :-) )
Removed Lups exhaust from the gunships, it looks bad, i realise now :)
Made the minesweeper weapon behave more elegant.
Added fixed scripts from krogothe86
Made Minwaterdepth of all big ships the same
Added luashockwave, Thanks jK!!
Mobile antinukes will no longer chase enemies
Altered the BA-Layout to 10 rows so it works better on 1024x768
Made Anti-nukes faster.
Fixed Seismic rings.
Amphids are as fast underwater as they are on land


6.0 → 6.1
03/02/2008

Updated CustomFormations widget, Thanks jK
Added the reclaim info widget
Added Exhaustflames to planes using LUPS, it looks nice now ~~
Added Collide=0; to all planes
Buffed the high traj weapon of the fido too, forgot that last release
Improved Shields
Fixed the Krow script, thanks [Krogoth86]!
Arm Marky can be build again (fixed a typo)
Core Tidal is as small as Arm Tidal now
Added ARM.bmp and CORE.bmp to sidepics for support with other lobby's
Intimidator shots cost the same as Bertha Shots now.
Fixed Nuclear Missles / Starburst Missles.
You can no longer FPS Vipers, Tactical nuke Launchers.
Added AreaAttack to Arty-veh, Bertha/Timmy
Radar/Jammer units will no longer "attack"
Added a Layout for the Gui , a widget by lurker, many thanks!


5.91 → 6.0
02/01/2008

Updated defenserange widget by verybadsoldier
Updated LUPS
Updated HP-bars widget by jK
Fixed Arm HoverConstructer script, Thanks Krogoth86
Decoy Commanders wear Santa Hats too now(when its christmastime)
Increased LOS of Radar Veh/kBots
Increased Zeus HP
Increased Fido Range
Increased Maverick HP
Increased Fatboy HP and DPS
Increased Pyro DPS
Core Battle Sub no longer drains E
Both Battle Subs have increased turnrate now
Decreased Arm Seabomber HP
Shiva no longer targets planes
Removed specialdamages from T1 subs to Torpedo Launchers
Increased Shields repulsionstrength
Added modtags to modinfo.tdf
Buffed Advanced Torpedo Launchers, Less costs, more HP
Increased Battleships HP and Range
Torpedo Seaplanes are in the L2bombers Armorclass now 
Removed MetalGenerators
AF fixed unit_direct_control.lua, Thanks!
Fixed Starburst Missiles (e.g. Merl and Nuke) to work with SVN version


5.9 → 5.91

Fixed Corssub corpse metalvalue
Added missing files for the Healthbars and the defense range widget.
Removed unneeded tags for the VTOL_SABOT and the VTOL_ROCKET weapons
Buffed Arm Zipper's HP and DPS
Plane Trails disabled for now, Spring doesnt displays it properly IMO, at least not with lups.
Increased LoS of Flea and of AK, so they can be used as LLT spotter for Storm/Rocko
Added the V for the version again :P
Added the latest Defenserange widget


5.8→ 5.9
04/12/2007

Added Defense Range V3.1, by verybadsoldier
Added Healthbars widget by jK
Added Customformations widget by jK
Added unit_mex_upgrader.lua by BigHead
Increased Juggernaut's Mass
Decreased Sumo's range, this also effects MohoExploiter and Doomsday machine
Nukes will no longer collide with Friendly units (so it wont go BOOM above your base, when it hits a fighter :P)
RadarVehicles LOS adjusted, ARM nerfed, CORE buffed >:)
Added an image needed for the buildbar widget.
Commando noautofire=0; now, also decreased the EMP damage so it shouldn't cause heavy screenshakes. Also doubled its capturespeed =)
Fixed Rapier and Blade missile's
Arm Destroyer slighty more DPS (7%)
Nerfed Doomsday Armour 5% to 8%
Consul begins building faster now, thanks Krogoth86
Added avoidfriendly=0; to the DGun
Reduced Special damage from LRPC/RFLRPC's to ships
Ships/Subs wrecks leave a Heap now when they get destroyed.
Fixed CorConship/CorRoy wakes.
Replaced Adv Fusion models with the CA models, Thanks Saktoth
Added Some lights on some factory's a la CA.
Added LUPS, which adds some effects to certain units, Many thanks go out to jK for making LUPS
Necro and rector will leave a corpse now.
Removed corpses which aren't needed.
New set of Loadscreens
Disable FPS control of the Moho Exploiter
Buffed Intrusion Countermeasure System's

Redid T2 sea (will still require more tweaking probally =)):
Levithan/Serpent are Battle subs now
Sharks/Piranha's are Sub Killers now
Cruisers costs Increased, Depthcharge Nerfed
Flagship Range Increased.
Naval Assister worker time Increased
Reduced Costs of Anti-Air ships
Seaplanes got more like T1.5 stats now and can submerge.


5.71 → 5.8
30/09/2007

Light mines really don't do impulse anymore.
Reverted Gater Hitsphere
Transportships can no longer load enemy units.
Juno Weapon will no longer kill fusions on maps like SpeedBall and Cow.
Reduced Tremor costs (20%)
Increased Reaper DPS (15%)
Increased Reaper Weapon velocity
Increased Goliath DPS (30%)
Reduced Goliath max speed (20%)
Reduced Goliath Turning speed (30%)
Increased metal worth of Gol Corpse
Increased Goliath HP (16%)
Reduced Penetrator DPS (10%)
Reduced Bulldog DPS (10%)
Increased Panther DPS (35%)
Decreased FHLT range
Increased Bertha/Intimidator accuracy
Reduced Catalyst costs
Reduced Catalyst Range
Reduced Catalyst missle Costs and Buildtime
Increased Destoyers Range
Increased Missle Hover range 
Increased Aircraft Carrier Ships worker time, to match repair pads.
Changed Maverick's description to Skirmish Kbot


5.7 → 5.71

Fixed the wreckagefile


5.61 → 5.7

Arm Spy can no longer be build from the Amphid lab.
Really fixed the Arm Seer corpse metal ammount :P
Removed the radar turn off on E-stall lua-rule.
Increased Buzzsaw/Vulcan energycosts to fire, you need redicoulous ammounts of E now :)
Floating targetting facility's costs divided by 4, so they are in line with the landbased ones.
Arm Solar Hitsphere decreased to Core Solar size
Gator Hitsphere decreased to Armflash size
Tweaked Floating Radar hitsphere's so subs can kill them more easy
Light mines no longer do impulse
Removed Flares from all planes which had them
Made Juno Cheaper, Moved to T1 builders, Made the missle cheaper, faster to build, decreased its AoE a bit (You can also kill minefields with it!!!)
Radar Jamming Kbots have the Kbotmovementclass now.
Added one boring loadscreen, because Satirik Bribed me :(
Increased Catalyst's Range, reduced the damage to commanders


5.6 → 5.61

Fixed typo which caused the Core Adv Kbot lab to be 10 times expensive as it should be.


5.5 → 5.6
22/08/2007

Increased Juggernaut's Size, and costs
Put the Juggernaut in the Krogoth armor class, so it receives the same special damages
Maverick leaves a wreck now
Informer and Seer wrecks metal worth adjusted.
Increased Halberd's size, and fixed the firepoint, Saktoth fixed the script
Juno's Missle Now also destroys minefields
Increased Ground damage of Avengers and Freedomfighters
Increased Sonar Range of Destroyers a bit
Triton costs reduced
EMP-bombs damage reduced, to fix the screenshaking if you use the screenshaking widget
Added some gfx to some units, took from XTA and modified them a bit to fit BA, thanks Noruas and Gizmo!
Improved Vulcan/Buzzsaw's accuracy, but it takes a shitload of E now :)
Fixed bladewing patrols, thanks to Saktoth
Jammers/Radars now disable when you E-Stall, lua script by licho
Made Juno's weapon go less high
Dragon Eyes can no longer be build in the water
Spies are no longer amphib
Pelican a bit more hp and dps
Core skuttle is now amphib and cost some less BT
Increased Viper/Pittbull costs a bit
T2 Factory's cost less now
Replaced the loadscreens


5.4 → 5.5
21/07/2007

Massivly increased Juggernauts HP
Increased Bantha's HP
Increased Razorback speed and dps
Viper and Pittbull DPS doubled
AK speed incresed
Increased Merl/Diplomat AoE and DPS
Doubled Tremor costs, well almost.
Doubled Krow's HP
Almost halved Liche's costs
Increased Banisher DPS
Added some lua widgets


5.3 → 5.4
06/06/2007

Storm costs increased
Reaper hp increased
Warrior dps increased
Cor goliath costs increased
Samson/Slasher LoS increased
Panther is more accurate now while moving
V-launch missles don't go as high anymore


5.2 → 5.3
22/05/2007

Janus range reduced, dps reduced.
Fixed the movementclasses of radar/jammer veh/bots.
Rez bots moved to T1 Kbots. costs adjusted.
Decreased Thud and Storm costs slightly to make up for armwarrior.


5.1 → 5.2
16/05/2007

Fixes a bug which might cause crashing when building and adv factory.
Removed streak (Caydr's bonus unit)
Bantha can no longer be airlifted
Made some buildpics a bit brighter (Thanks Trademark)


4.7 → 5.1

Flash slowed down a little
Energy structures revised, each step is now like a 30 % efficency gain Solar -→ adv Solar -→ Fusion -→ Adv Fusion. The underwater fusions have the same efficency as a regular fusion. The cloaked fusion is about 20% more effective then adv solars.
Snipers are no longer stealth
ARM mohomines lost their cloaking ability.
Fixed Seaplane torpedo planes, they will fire on ships now, they lost their anti air missle in the progress though.
Fixed bladewings, they will keep attacking units now.
Added back in the mobile radar/jammer vehicles/kbots, their costs adjusted to make more sense.
Reverted Arm Dragon Teeth model.
DragonTeeth have a higher slope tolerance now.
leveler reload time decreased slightly
janus damage increased
Commander Self-D time reduced to 5 seconds.
beamers damage improved 
claws/maws damage improved
claws accuracy improved
Gave the corvette ships some more speed and dps

T2 got buffed, Day took some time to tell me how he did it:

Core 
reaper role changed into more of a lighter tank
golly firing rate increased weapon damage increased aoe increased
pillager made faster, costs increased
mobile flak firepower reduced
can dps and speed increased
sumo range and speed increased
dominators a little more firepower
made crawling bombs faster
Pyro a little faster

Arm
zeus faster, more health
fido speed increased slightly
sniper stealth removed
crawling bomb faster
fatboy more range
mavs a little faster
zipper a bit more health
bulldog made faster
penetrator shorter reload
luger faster, costs decreased
panthers a bit faster


4.61 → 4.7
01/03/2007

Fixed Vamp Cruisealt
Intruder can no longer load enemy units (Thanks Rattle)
Implented Argh's Arm DT (someone should make us some for Core too. and maybe the floating DT's fortwalls as well)
T3 units are no longer transportable.
Seaplanes fighters do damage to aircraft again
Added some effects by Fox
Added Decoy tags so they won't be broken with luaui
Juno costs (M/E/BT) reduced by 30 %
Croc DPS reduced by 20 %
Skuttle damage and AoE improved by 20 %
Repairpads are no longer transportable
Repairpads are 30% cheaper
Fusions have their stats hidden to the enemy now, so decoys work
Decoy Dgun costs 50 E to fire now instead of 500
Maverick speed increased by 15 %
Lvl2 Radar Jammer E Costs to about 18K instead of 1.8K


4.6 → 4.61

Fixed minelayer's Sweep weapon (hopefully)
Gunships/Transports/Some other planes are no longer near immune vs fighters.
Commado can no longer cloak
Improved Corvette's tracking it's like a LLT now.
Skeeter/Searcger HP nerfed


4.5 → 4.6

Core radar has LOS again
Stumpy speed reduced (its slower then a gator now, but still faster then a raider)
Gave Corvette's Lazors, Lowered DPS a bit because it will always hit now.
Sniper cost to fire is 500 E now.
AK 40 less HP
Removed special movementstats of Hawks/Vamps/Seaplanes
Reduced grouddamge of all fighters to 30 % to ground targets, 10 % to Commanders
HLT's 5 % more DPS
Hoverscouts 15 % more costs and BT
Bombs do 50 % less damage to chainsaws (adjusted their description)
Thuds/Hammer DPS increased by 6%
Floating dragonteeth can be reclaimed again
Fixed EMP problems (Thanks Saktoth!!)
KrogCrush will do even less damage to heavy units.
Fixed banisher visual bugs (Thanks Nemo!!)
Fixed typo in the torpedolauncher weapon. It will have a lower ROF now.
Improved Minesweeper (bigger AoE) and gave it a visual effect, just force fire somewhere.
Fortwalls can be reclaimed now, but they have 200 E, so they reclaim slow about 3 seconds a piece.
Removed the AoE of depthchargelauncher's weapon, it shouldn't be OP anymore on Tropical like maps


4.41 → 4.5
08/01/2007

Fixed the metalammount of the Targeting facility's corpses and heaps
Gave Janus its "arc" Weapon as in AA
Decreased Doomsday Costs by 30% (also adjusted corpses)
Increased Doomsday HP by 11%
Made radar planes, Radar/Sonar planes
Arm Blade (Level2 Gunship) will no longer chase planes
Greatly reduced the bugginess of skeeters/searchers to fire their AA missle.
Corpse of Hive no longer floats
All seaplanes have floater=1; now, so they can land on the water
Seaplane radar/sonar planes, sonarrange doubled.
The advanced Construction subs are deeper in the water now, so their buildturret will not come to the surface.
Decreased Core Mohomine costs/builtime/corpsevalues to match the Arm version more.
Made the lasers thicker and more colourfull.
Vamps/Hawks Flare reloadtime increased by 40%, grounddamage reduced by 10 %
Seaplanes can now be build by L1 Con Ships
Seaplaneplatform costs increased by 20 % (and corpse)
Juggernaut costs reduced by 10 % (and corpse)
Pelican maxvelocity increased by 30 %
Gave NavalEngineers more buildpower
Seismic detectors costs Halved (and corpse)
Made the Destroyerships able to fire while retreating/turning.
Underwaterfusions produce more E now, they are on par with regular fusions now
Floating metalmakers make 1.1 metal per 60 E now
Underwater Mohomakers make 13 metal per 600 E now
Increased adv sonar range to be more inline with the regular sonars
Removed HAX rangerings as they are no longer needed
Included a somewhat GUI, you have to enable LuaUI in settings.exe (gui.lua was made by Napkin, Thanks!)


4.4 → 4.41

Fixed Geo's
Minelayers will no longer follow enenmy units


4.33 → 4.4

Advanced Anti Air Kbots and AA hovers no longer follow ground units
Gave detpcharge some tracking again
Fixed the extraction rates of mexxes/twilights/exploiters, somehow they were mixed up
L1 Arty can shoot up hills again, due to faster weaponvelocity and hightrajectory
Floating radars can no longer be build on land
Adjusted sonar range rings, so that they reflect the real range
Builtime of Estorages reduced by 50 % (this included the underwater ones)
Reduced Ecosts and Builtime of the Juno by 20 %
Gave the Minelayer some AoE weapon, you still have to manual "attack" the enemy minefields


4.2 → 4.33

Arm Fusions really makes 1000 E now
Core Fusions really makes 1100 E now
Adv Fusions really make 3000 E now
Tremor got less hp now
Fixed Sniper bug
Took Commanderscripts from XTA and made the movement of the "Arms" faster
Targeting facilities cost 1/4 now, more facilities will enhance your accuracy of radar dots
removed arrival sounds
Added some loadscreens, thanks machio.
Reduced hp of scouts hovercraft
Floating metalmakers cost 1 metal now
Reduced Gator maxspeed
Reduced acceleration and turnrate of destroyer ships
Removed the laser off the Destroyer ships
Made the depthcharges no longer tracking
Fatboy costs reduced by 30 %
HLT's DPS increased slightly
Increased Banshee DPS slightly
Advanced Anti Air Kbots no longer chase ground units.
Increased leveler E costs
MT/PackO's do 10 % less damage now
LRMT reloadtime increased
Increased Acceleration and turning of Luger/Pillager
Thud/Hammer now have LoS till the end of their range
Increased Solar Buildtime 
Halved JellyFish E-costs
Tidal E costs Halfed
Reduced Torpedo Launcher E Costs by 30 %
(Adv.) Sonar range Doubled
Torpedo from subs have some guidance now
Poison Arrow moved to a other moventclass, so it can climb steeper slopes
Changed the maxslope of shiva in the FBI so it matches with the movementclass
Increased Beamer DPS by 5 %
AK speed reduced a bit
Improved the Core Maw in hp/dps/weaponspeed
Core Slasher's HP bar is now visable when he fires
Made Krogoth Able to Crush units with his feet, except heavy units/buildings
Gave Krogoth more HP
Reduced E Costs of All T3 units by 40 %


4.1 → 4.2

Fixed EMP bomber damage (it will only do stunning now)
Punisher now has the correct icontype
Mohometalmakers rebalanced
Floating metalmakers rebalanced
Added Level2 AA bots back in
Added a D-gun effect borrowed from XTA8.1
Increased Advanced radar ranges slightly
Increased Floating radar ranges slightly
Matched radar ranges to dummy range
Arm and Core Geo both produce 300 now
Arm and Core Moho Geo both produce 1250 now
Fusions make 1000 E now, ARM 4000 HP CORE 4500 HP
Adv Fusions make 3000 E now, ARM 7500 HP CORE 8500 HP
Banisher range reduced a little
Weasel/Jeffy reloadtime increased a bit
Conveh and Conbot buildspeed the same now (90)


4.0 → 4.1

Fixed a panther bug
Added custom unit icons


3.0 → 4.0

AK speed reduced Health increased range increased damage reduced
Penetrator range increased
Fixed dgun being able to fire 3 times at once
Fixed a typo in merl health
Thunder/Shadow health and turnrate increased significantly
Reverted tremor damage
Zipper E costs lowered
Fixed panther speed bug
Dominator costs increased to match its increased range
Weasel/jeffy E costs lowered (for some reason it was 600ish)
luger/pillager damage increased and aoe increased ( just trying to make this unit usefull instead of removing it)
Freedomfighter/Avenger costs increased slightly
Bladewing costs reduced
Banisher range increased
Advanced solar (core&arm) E costs reduced (not 0)


2.23 → 3.00

Flash/Instigator health reduced
Stumpie/Raider costs reduced acceleration increased projectile speed increased
Samson/Slasher costs reduced damage increased slightly
Wolverine/Shellshocker range increased
Weasel/Jeffy health and damage reduced
Construction vehicle workertime decreased
Leveler costs reduced damage increased speed increased
Peewee speed increased
Construction kbot workertime increased  it now builds faster then the construction vehicle
Rocko/Storm damage increased slightly maxspeed increased slightly
Hammer/Thud damage increased slightly
Warrior energy costs reduced
Flea now has a blowtorch! (actually its a bug i cant fix, im a noob modder!)
Tier one Kbot lab metal costs reduced
Solar now only costs metal
Wind energy cost increased slightly
Can damage increased slightly (3%)
Morty costs reduced (spam baby spam)
Pyro health increased slightly
Dominator range increased (it now actually outranges Vipers! and lots of other stuffs)
Maverick health reduced (you can get the fuckers by doing lots of damage at once so the regeneration doesnt have a chance)
Reaper/Bulldog range decreased
Merl/Diplomat health decreased alot! (i honestly dont know why an artilery unit like that had 3k health)
Luger/Pillager now fire at low trajectory with increased damage 
Panther health reduced
Tremor damage increased slightly
Brawler/rapiers now have 1k health
Banshee damage increased (20%) E costs reduced




2.22 → 2.23
20/10/2006

Absolute Annihilation, the game BA was based on.
