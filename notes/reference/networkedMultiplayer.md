# NETWORKED MULTIPLAYER

## https://www.gamedeveloper.com/programming/the-lag-fighting-techniques-behind-ggpo-s-netcode; last accessed: 20220915

### Previous Technique

> Aside from making sure the game runs deterministically, the engineers and designers implementing the gameplay can be isolated from the details of the network engine. This means you can retroactively add online multiplayer support to games that have already been released. (If you can provide a machine emulator for the original hardware the game was written on, you don't even need to recompile it!) 

### Problem

>  Unfortunately, this method also comes with one major drawback: These games are usually designed to sample the controller input before every simulation state update. A simulation frame in the game cannot execute until all the inputs from remote players have been received. In practice, this manifests itself as an input delay equal to the time it takes to send a packet from one console to the next. In short, the games lag. 
 
### Solution

### GGPO Netcode =  "Good Game, Peace Out" Netcode

> Instead of waiting for all inputs to reach a player's simulation before executing a frame, GGPO will guess what remote players will do based on their previous actions. This eliminates the lag experienced by the local player created by the traditional frame-delay method. 
 
### keyphrase: ACTION RECORDING; continuous RECORDING OF PLAYER'S GAMEPLAY
 
>  When GGPO receives the remote inputs from the network, it compares the predicted inputs to the actual ones. If it finds a discrepancy, it rewinds the simulation back to the first incorrect frame, repredicts the inputs for each player based on the updated input stream, and advances the simulation to the current frame using the new prediction.
  
### notes: PRE-LOADS NEXT ACTION,   

### reminder: select 3D object files in megabytes
  
### question: 2D only object fighting game also?
  
