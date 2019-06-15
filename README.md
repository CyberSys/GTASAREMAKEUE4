# grandtheftautosa
Readme is WIP

Pepare the Project:
-  before opening the project for the first time enable the LPV by following this doc: 
   https://docs.unrealengine.com/en-US/Engine/Rendering/LightingAndShadows/LightPropagationVolumes/index.html
-  In the project settings control and/or adjust the following settings:
    *Navigation Mesh -> Runtime Generation: Dynamic
    *Navigation Mesh -> Fixed Tile Pool Size: Enabled

jobs and dependencies:
1. global clock
    -timecycle
    -weatherzones (zones the player is on + the ability to see overcast weather in country/san fierro region
    -time depending spawning of peds
    
2. ai:
    -popcycle, evenly scattered ped spawn depending on popcycle, pedgroup and zone
    -spawn in different conditions (walking, possessing different vehicletypes like cars, boats...)
    -give peds a task (walk to a certain place and eg. make them do something
    -ai acquaintance (LIKE, DISLIKE, HATE...) other pedgroups
    -every event (shooting, stealing...) and pawn sense of peds and the player trigger an event
     on the ped. eg. when any pawn in the world shoots all surrounding peds (eg. via a sphere trace to cover 
     an area around it and alarm all peds inside it) get alarmed and based on a decision file act different, one 
     might flee/get to cover, shoot back etc or follow a more complicated structure.
    
3. vehicle:
    -implementation of well manouverable vehicles (cars, planes, boats, bikes, motorbikes, helicopter, trucks with trailer)
    
4. advanced customization/buy system  
    -ability of player to buy and afterwards access properties or access properties of friends by invitation
    -shop system (clothing, weapons, food, haircuts, tattoos
    
5. Missions
    -fully coop supporting missions to up to 4 players
    -mission events like races, team deathmatch, capture the flag for up to 32/64 players
    -sidemissions like burglary, pick pockets, taxi, vigilante...
    
6. full multiplayer support
    -dedicated server system + browser (preferred over lobbysystem because of serverside operations 
     that consume too much clientperformance) 
    -ability to 'phone call' other people on the server using cj's phone 
     (just a medium of communication besides the chatbox and also misuse of the animations) 
    
7. weaponsystem
    -working system for shooting and aiming using ikbones
    -working driveby's from any seat in a car either as driver or passenger
    
8. weathersystem
    -good looking clouds that are not too performance heavy and can obstruct the clear view from on city to another 
     (eg. raymarch clouds, meshbased clouds, further testing needed)
    -working water surface with proper waves, reflections and collisions 
     (eg. GTA 5's water is definitely okay and a good compromise)
    
9. User Interface
    -proper User interface that is intuitive but matches the early 90's and the original game
    
10. player controller
    - the player controller has to be changed to be the 'god' of an ai controller. this means the player is automatically
      possessed by an ai controller from the beginning of the game and then a player controller gets the ownership of the player              
      pawn and 'sends' his actions to the ai to execute 
      (idea in this post explained: 
      https://answers.unrealengine.com/questions/374052/is-it-possible-to-use-both-ai-controller-and-playe.html
      this allows us to use ai specific function on the player such as 'ai move to' when eg. entering buildings, 
      vehicles and basicly force the player character to force the player to move to a goal location.
      
11. audio
    - the audio system shall be changed to the steam audio system that allows us to use reverb sound: 
     https://valvesoftware.github.io/steam-audio/doc/phonon_unreal.html . If someone knows a better system which similar 
     and/or better features feel free to implement it.
     
      
