# The Hollowing

A first-person horror game built in Unity (C#) that won first place at a game development hackathon. The twist: your own microphone is the main threat. If you make too much noise, the game ends.

This repository contains the game's C# scripts only. Scenes, models, audio and third-party asset packs are not included.

## Story

Five years after his sister Lilly was taken by a dark entity, Jonathan gets a voice message from her telling him to stay away. He ignores it, crashes his car near a forest town at dusk and has to continue on foot. Lilly's soul has been split into five artifacts, and she can hold the demons back for only six minutes. The player has to find all five artifacts in that time without making a sound.

## Gameplay

- **Microphone-sensitive gameplay:** a mic meter reads your input. A loud sound triggers game over. The sensitivity is calibrated on the instructions screen.
- **Stealth and chases:** demons hunt the player, with scripted jump scares and chase cutscenes. Sprint, lean-back camera and a flashlight with a draining battery are the player's tools.
- **Objective system:** a ringing phone unlocks the six-minute timer, and a direction arrow guides the player to the next artifact.
- **Win and lose:** collect all five artifacts before the timer ends, or lose to a demon or to noise.
- **3D positional audio** for footsteps, whispers and growls, best played with headphones.

Controls and the full description are in the [game guide](docs/the-hollowing-game-guide.pdf).

## Code overview

```
Assets/Main/Scripts/
  Audio/          microphone input, calibration, loudness meter, death handling
  Core/           event manager and shared helpers
  FPSController/  character controller
  Gameplay/       story flow, timer, quake and jump-scare triggers, end sequence
  Ghost/          demon chase AI and cutscene triggers
  Interactables/  artifacts, batteries, flashlight and phone pickups
  Navigation/     waypoint arrow guiding the player
  Player/         movement, flashlight, battery HUD
  UI/             menus, intro and outro, pause, pickup messages
```

About 50 scripts in total.

## Tools and credits

The game was built with AI assistance, as the game guide discloses: ChatGPT for scripting help and story brainstorming, Sora, ElevenLabs and Hailuo AI for visuals, voice and cutscene material, and Filmora for editing. Game design, integration and testing were done by the author.

The environment used in the game comes from a third-party Unity asset pack, which is not included here and is not covered by this repository's license.

## Building

The Unity project is not in this repository, so the game cannot be built from it directly. To use the scripts, add them to a Unity project (the game was built with the Cinemachine package) and recreate the scenes.

## License

MIT for the scripts, see [LICENSE](LICENSE).

## Contact

Anubhav Gupta, [LinkedIn](https://www.linkedin.com/in/anubhav-gupta-92410a244/)
