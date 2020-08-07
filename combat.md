# Combat

This is a description of combat and how it works with in this game.

## Architecture

Instead of player and AI managing damage directly, damage nodes and damage detectors nodes will manage the interaction.

### Damage Emitter nodes

This sends a damage signal to any **damage detector** node it interacts .

- Damage modes
  
  - **Continuous** applies damage at a set interval while node is in range.
  
  - **Once** only applies damage once, when the node is first detected.

### Damage Detector nodes

Detect when it has taken damage and outputs a damage taken signal

- **Returns**
  
  - direction that attack comes from
  
  - knock amount

## Physics Layers

both nodes are on **layer 10** and only layer 10 of the physics layer.


