# Drone Commander
You have been chosen to develop a new flying drone which can understand the 3D Cartesian coordinate system. It maneuvers in precise 1m increments in 3D space. A drone at (0,0,25) is 25m above the origin (0,0,0).

### Instructions
Create an interface for sending commands to the drone and displaying the drone's response.

## Drone Spec
### Valid Commands
The drone responds to the follow commands.

| Command | Description |
| ------- | ----------- |
| `l`     | Rotate left 90 degrees |
| `r`     | Rotate right 90 degrees |
| `f`     | Fly forward 1m |
| `b`     | Back up 1m |
| `u`     | Hover upward 1m |
| `d`     | Hover downward 1m |

### Crash Detection
If the drone receives a command which will cause it to touch the z = 0 plane after take off, it will crash. You should return the last known coordinate and cardinal direction to help locate the crashed drone. You can safely assume that there are no other obstructions in the air.

## Examples
| Start Coordinate | Start Direction | Commands | Drone Response |
| --- | --- | --- | --- |
| (0, 0, 0) | N | `uufrfflfdb` | "I'm at (2,1,1) facing N" |
| (5, 10, 2) | E | `frfdfdfu` | "I crashed at (6,8,0) facing S" |
