introduction

many actions, relationships or information are stored inside .csv files. They are found in *data/ .
to create a file you can simply follow these instructions:
https://docs.unrealengine.com/en-US/Gameplay/DataDriven/index.html
These instructions don't cover all information but it is possible to import color-,vector-and scalarcurves, gameplay
data, reference all kinds of files that are available in ue4.

performance
it is blazingly fast to iterate over the data tables, having thousand of rows inside a data table is no problem, 
it is lazily loaded, thus allowing to load just specific information or assets.

example usage

example 1 
cause referencing assets inside those files is easy as pie you can spawn any pawn in the world by 
using commands/name variables. eg. *data/bp_parked_car_generator has the function *set_parked_car that takes in
three variables:
'name' (desired car)
'vector' (spawn location)
'float' (spawn z-rotation)
it spawns any car that is referenced inside the file *data/vehicle/dat_vehicle. the blueprint is position in the persistent
world and can be triggered from anywhere, thus cars that are spawned this way are also spawned in the world and are not 
depending on the level streaming system. the car might not spawn in levels that are unloaded are fall through the world as soon 
a sub level gets unloaded because of missing collisions. in future a kill volume shall take controll over this to destroy such
a pawn or the pawn shall be unloaded if too far away from all players.

example 2
in*data/ped/dat_peds every pedestrians mesh, material and texture is referenced. this way by spawning a *peds/blueprints/bp_ped 
and initialize it with the function (currently an event) 'InitializePed' which takes in a 'name' variable the right mesh /texture/material gets assigned to the ped. This 
way you can use one mesh and assign every material you want that is referenced in the datatable. Also other properties get
assigned to the ped that define behavior, animations and optics of the ped pawn.

example 3
you can store a huge amount of data into the data tables as seen in *data/Paths/* every file stores, defined by it's corresponding
structure, many repeating data patterns and makes them available for a fast lookup. This way around 150.000 lines of data can be 
evaluated within a second. here many nodepoints completely covering san andreas andreas, compiled down to these files, are 
searched by specific conditions to find a route to a target location that can be eg. set by the user through the userinterface
or a function.
