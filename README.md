#AsteroidMining
##A hard sci-fi turn based real time strategy programming game

##Gaming as social and intellectual experience
The fascination and depth of good real time tactics and turn based strategy games comes from the fact that you need to outsmart your opponents. This kind of fun emerges in a social process of learning, communcating and improving. Thus even losing is not frustrating, but encouraging. Unfortunately, most of these games require a lot of manual micro management, a high frequency of interaction and often have a monotone opening, such that motoric skill and speed influence your success more than creativity and intelligent decisions.

##Programming for abstraction
We want to think about a strategy game that specifically allows you to have a _sophisticated_ strategic expericence. Where you can abstract away all manual interaction once you consider it boilerplate and instead concentrate on more interesting higher level challenges. Programming, as intimidating as it may sound, is the right tool for this kind of interaction model.
Therefore the experienced level of complexity is mostly user-defined, and we can afford the game to have extensive simulation features without necessarily overwhelming players with detail, but instead present them growing challenges in a believable environment.

##Turn based real time strategy
To enforce thinking instead of mindless action, we introduce a latency between command and execution like in turn based games. But since the simulation continues to run independently, players can choose the amount and frequency of ineraction depending on their interests and the task at hand.

##Hard sci-fi
A scenario which perfectly fits our goals in terms of game experience, is an asteroid mining operation conducted by programmable robots. We want hard sci-fi - things that are fascinating to think about and entirley possible, but just didn't happen yet. No aliens, no interstellar travel, just plain old space exploration in all its glory and with all its physical constraints.

##Project scope
The goal is to outline and prototype a minimalistic framework that runs the game on a server. It can be addressed by clients who send their drones direct commands or software to run, and then get back sensor feedback with appropriate delay. The server provides and manages environment information like terrain data, sunlight exposure or resource locations. Since communication will most likely be simply based on byte strings, users can choose their own form of representation and for example generate maps, graphics and animations from the information they get back. 

An initial multiplayer game mode could consist of at least two players starting on the same rock at the same time, with chosen configurations. Drone setup influences return on investment, since different components determine mission cost and duration. The goal is to be first sending his drone back profitably, because market prices for a given resource will drop significantly on arrival and destroy the late opponent's business.