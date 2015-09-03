# A few ideas for a prototype

## Environment

A game server provides an invironment for robots to operate in.

This could for example be a simple 2-dimensional map with square fields each containing some amount of a resources. The robot can move in 4 or 8 directions. If it has the right modules available, it can request information about the map field it stands on and also interact with it, for example by mining some resource. Resources could be all the nice things that are known to be up there (see [References](references.md)).

If the environment recives a message from a robot, it checks in the game state whether the robot actually has the referenced module and the action is valid. Then it updates the game state and informs the robot when the task is done. The returned information could be a string and empty if the request was invalid.

## Robot

A robot is presented to the user as a remote computer with hardware interfaces, which is simulated by the game server. Users can provide the robot with a program, which is then run according to server constraints. These can be due to policy (like granted CPU time and memory) as well as game rules (only some actions are allowed in specific situations).

The running robot program can now interact with the environment. This interaction either using strings or some other API (since it's only a prototype maybe strings are easier).

For example, the robot sends a reference to the module which shall be used and which action to execute on the environment. This call is checked for validity by the server and then passed to the environment. The robot then can compute what to do with the information it gets back.

## Robot modules

A robot consists of a main frame where modules can be attached via a limited number of interfaces with various constraints. These modules could include
 * Antennas with different reach and bandwidth (necessary to commincate with user)
 * Stations (a refuge and storage place, maybe it can also lift off and transport expensive things back to earth)
 * Storage containers
 * Arms with different strength (can lift objects, a shovel and cargo space might be liftables)
 * Wheels and motors with different speed
 * 3D printer with different abilities to print other modules from materials and energy.
 * Energy producers (solar, nuclear)
 * Energy storage
 * Microcontrollers with different CPU and RAM
 * Weapons
