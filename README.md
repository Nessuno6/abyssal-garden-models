# Abyssal Garden: models

Animated 3D models for [Abyssal Garden](https://github.com/Nessuno6/abyssal-garden), the endless procedural
underwater world. In the game, **Models → Library** lists this repository and adds a model in one tap. You can also
download a `.glb` from `models/` and add it with **Models → Add models**.

* `models/`: the game-ready files (binary glTF with skin and animations, textures embedded, at most 2048 px).
* `blender/`: the Blender files they were exported from.
* `manifest.json`: what the game reads. It lists each model's file, class, animation clips, author, source and
  licence.

## Licences

**The models are not under one licence.** Each keeps the licence its author chose (below). This repository has no
licence of its own over them; the game's code is MIT, in its own repository. Credit the authors as below when you use
a model, and say that it was changed (rigged, animated, converted).

| Model | Class | Clips | Author | Licence |
|---|---|---|---|---|
| [Creature Evolution #2](https://sketchfab.com/3d-models/creature-evolution-2-4d9437b8758544c9a5d47854b84038e7) | creature | swim, fast, idle, turn | [alexalbinyana](https://sketchfab.com/alexalbinyana) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| [Reaper Leviathan](https://sketchfab.com/3d-models/reaper-leviathan-dfbe936f6fcb40f79bef4d0de6d83a27) | leviathan | swim, fast, attack, roar, idle | [patrat623](https://sketchfab.com/patrat623) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| [Subnautica: Hydra Submarine](https://sketchfab.com/3d-models/subnautica-hydra-submarine-a0ede1b5e7034d1aa67a14cef7b797be) | submarine | cruise, idle, turn | [Aci](https://sketchfab.com/Aci_yt) | [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) (**non-commercial**) |
| Hydra Submarine: cockpit and command centre (new, made for Abyssal Garden inside the Hydra) | submarine interior | | derivative of Aci's Hydra | [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) (**non-commercial**) |
| [Diver](https://sketchfab.com/3d-models/diver-9ee9b8b722ed457da424869cd8d08b1a) | player | idle, swim, fast | [nolanfa](https://sketchfab.com/nolanfa) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |

**Changes:** every model was rigged and animated in Blender for Abyssal Garden. The materials were converted to plain
metallic-roughness, and large textures scaled down to 2048 px.

**Non-commercial:** the Hydra and its interior are CC BY-NC 4.0: do not use them commercially.

**Note on fan models:** the Reaper Leviathan is a fan model of a creature from *Subnautica* (Unknown Worlds
Entertainment). Its Creative Commons licence covers the modeller's work, not the original game design, which belongs to
its owner. It is shared here for non-commercial fan use.

## Adding models

1. Add the `.glb` to `models/` (and the `.blend` to `blender/` if you have it).
2. Add an entry to `manifest.json`: `name`, `file`, `class` (`s` structure, `p` plant, `c` creature, `l` leviathan,
   `m` submarine, `b` boat, `i` submarine interior), `clips`, `title`, `author`, `authorUrl`, `source`, `license`,
   `changes`.
3. Add a row to the table above.

Clip names the game reacts to:

* creatures: `swim`, `fast`, `idle`, `turn`;
* leviathans: `swim`, `fast`, `attack`, `roar`, `idle`;
* submarines: `cruise`, `turn`, `idle`.

A submarine interior is named `<submarine name>_interior` and is modelled in the hull's own frame, with marker empties
(`pilot_seat`, `hatch`, `hatch_inside`, `sonar`, `lights_panel`, `power_panel`, `repair_panel`, `passenger_1..3`,
`floor_min`, `floor_max`).
