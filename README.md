# Stacker Practice Simulator

A 3D browser simulator for practising the warehouse exercises from the Danish gaffeltruck (forklift) test, on an electric stand-on stacker.

Single file, no build step: open `index.html` in a browser. It loads Three.js r128 from cdnjs, so the first load needs internet.

## Exercises

- **Free drive:** no tasks or flags. Walls and racks just block you.
- **Tyre pallets, rack A to rack B:** 6 pallets from the deep rack (1 lane, 3 deep, 2 levels), turned in the metal frame, into the pallet rack (3 slots wide, 2 levels).
- **Tyre pallets, rack B to rack A:** the same exercise in the other direction.

Rack A is entered from the pallet's long side, rack B from its short side. The frame is where the side is switched.

- Rack A load order: bottom, top, bottom, top, ... deepest position first. Unload is the reverse.
- Rack B load order: bottom side, bottom side, bottom middle, then top side, top side, top middle. Unload is the reverse.

## Flags

- **Red (1 = out):** collision, or uneven stacking (sticking out, not centered, crooked, not flat).
- **Yellow (4th = out):** hard hit, wrong load or unload order, driving with the forks raised, pallet not turned in the frame, pallet put down outside the frame.

## Controls

| Key | Action |
| --- | --- |
| Up / Down | Forward / reverse (hold to build speed) |
| Left / Right | Steer |
| Space | Brake |
| R / F | Raise / lower forks |
| C | Camera: chase, operator, top-down |
| H | Show / hide the task hint |
| Enter | Restart the exercise |
| Esc | Menu |

## Not built yet

Ramp drill, reckless driving, mast tilt, reach truck, counterweight forklift.

## Notes

The flag thresholds (fork height, stacking tolerances, hard-hit speed) are estimates, not taken from the official course material. They are constants near the top of the script in `index.html`.
