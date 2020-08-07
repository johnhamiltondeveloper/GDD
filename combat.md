# Combat

This is a description of combat and how it works with in this game.

## Architecture

Instead of player and AI managing damage directly, damage nodes and damage detectors nodes will manage the interaction.

### Damage Emitter nodes

This sends a damage signal to any **damage detector** node it interacts .

- Damage modes
  
  - **Continuous** applies damage at a set interval while node is in range.
  
  - **Once** only applies damage once, when the node is first detected.

This node dose not collide with its own layer

### Damage Detector nodes

Detect when it has taken damage and outputs a damage taken signal

- **Returns**
  
  - direction that attack comes from
  
  - knock amount

This node collides with the emitter layer but not its own layer

## Physics Layers

- **Layer 10** - Damage Emitter - Layer used for the Damage Emitter nodes

- **Layer 11** - Damage Detector - Layer used for the Damage Detector nodes
