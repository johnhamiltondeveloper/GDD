# Combat

This is a description of combat and how it works with in this game.

- [ ] Add what a unit of damage means e.g. what dose "1 damage mean"

## Architecture

Instead of player and AI managing damage directly, damage nodes and damage detectors nodes will manage the interaction.

### Damage Emitter nodes

This sends a damage signal to any **damage detector** node it interacts .

- Damage modes
  
  - **Continuous** applies damage at a set interval while node is in range.
  
  - **Once** only applies damage once, when the node is first detected.

Collides with nodes on **layer 10** but is not on a layer it self, it can only detect collisions. 

### Damage Detector nodes

Detect when it has taken damage and outputs a damage taken signal

- **Returns**
  
  - direction that attack comes from
  
  - knock amount

This does not collide with other layers, but can be detected by the damage emitter on layer 10

## Physics Layers

- **Layer 10** - Damage
