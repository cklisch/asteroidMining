# A few ideas for a prototype

## Environment
1. A simple 2 dimensional map with square fields each containing some amount of a material. The robots can move
in 4 directions. If it has the right modules, it can request information about which material it stands on and also
mine it.

2. If the environment recives a message from a robot it checks in the game state weather the robot has the referenced
module and the action is valid. Then it updates the game state and informs the robot when the task is done.
The returned information is also a string and empty if the request was invalid.

2. Materials:
 * all the nice things that are know to be up there

## Robot

1. The main module for each robot is its microcontroller. On it runs a programm which was initially put there by the user.
It can recive new source code from the environment (send from the user) and switch between different programms. 
The program running can interact with the environment. This interaction either using strings or some other API 
(since only a prototype maybe strings are easier).

2. The robot sends a reference to the module which shall be used and which action to execute to the environment. It can 
compute what to do with the information it recives back, but only with a limited amount of memory and CPU time depending
on wich microcontroller it uses.

3. Objects:
 * Microcontrollers with different CPU and RAM
 * Antennas with different reach (necessary to interacts with the environment)
 * Stations (a refuge and storage place can maybe it can also ignite and transport expencive things back to earth)
 * Arms with different strength (can lift liftable objects: another robot, wheels,  a shovel and cargo space might be liftables)
 * Torso with different number of possible arms storage.
 * 3D printer with different abilities to print other modules from materials and energy.
 * Energy storage
 * Energy producers
 * Wheels with different speed (also attached to arms).
 * Weapons
 
