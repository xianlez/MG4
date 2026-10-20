# MG4
## Devlog

The FloatAnimation script makes the fish food GameObjects move up and down by alternating their movement direction.

Start() runs once when the component begins running. It sets _timer to _switchSpeed, which determines how many seconds pass before the movement direction changes. The boolean variable _up starts as false by default, so the food initially moves downward.

Update() runs every frame. When _up is true, transform.Translate moves the food upward along the Y-axis. When _up is false, it moves downward. Both movements use _moveSpeed multiplied by Time.deltaTime so the movement is based on elapsed time rather than the number of frames.

Each frame, _timer decreases by Time.deltaTime. When _timer reaches zero or below, the script resets it to _switchSpeed and uses `_up = !_up` to reverse the direction. Repeating this countdown and direction change makes the food continuously float up and down.
## Open-Source Assets
- [Quirky animal 3D models](https://assetstore.unity.com/packages/3d/characters/animals/quirky-series-free-animals-pack-178235)
- [City 3D models](https://assetstore.unity.com/packages/3d/environments/simplepoly-city-low-poly-assets-58899)
- [Bite sound effect](https://freesound.org/people/Jofae/sounds/353067/)
