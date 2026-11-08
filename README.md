# NPC Voice (Forge 1.20.1)

Spawn an NPC with the **NPC Spawn Egg** (Creative > Spawn Eggs), then talk to it with Simple Voice Chat.
The closest NPC within 32 blocks of you hears you.

## Voice commands
| Say                          | Effect                                              |
|------------------------------|-----------------------------------------------------|
| "follow me"                  | NPC follows you                                     |
| "come here"                  | walks to where you stand                            |
| "stay" / "stop" / "wait"     | stops                                               |
| "attack" / "fight"           | attacks nearest hostile mob                         |
| "spawn a player named Bob"   | spawns another NPC named Bob (uses `/player Bob spawn` if a mod on the server provides that command) |
| "go away"                    | removes the NPC                                     |

## Setup
1. Install on the server AND every client: Forge 47.x for 1.20.1, **Simple Voice Chat (Forge 1.20.1)**, and this mod.
2. Download a Vosk model (e.g. `vosk-model-small-en-us-0.15` from https://alphacephei.com/vosk/models),
   unzip it, and put its contents in `<server>/config/npcvoice/model/` (so `model/am`, `model/conf`, ... exist).
   In singleplayer that is `.minecraft/config/npcvoice/model/`.
3. Build (JDK 17): `gradle wrapper && ./gradlew build` -> `build/libs/npcvoice-1.0.0.jar`.
