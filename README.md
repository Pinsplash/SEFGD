This is a collection of brand new [FGD](https://developer.valvesoftware.com/wiki/FGD) files for Source engine games. FGD files tell Hammer what entities there are, and what settings, inputs, and outputs they have.

Most of the information in these files was rewritten from scratch by me to be more accurate, comprehensive, and easier to follow. A lot of things I've written in them are confirmed by in-game testing and checking code. New entities, flags, keyvalues, inputs and outputs were found by referring to [dumpentityfactories](https://developer.valvesoftware.com/wiki/Dumpentityfactories), [code resources](https://github.com/ValveSoftware/source-sdk-2013/) in many places on the internet, [Source.Python](http://wiki.sourcepython.com/), and [SourceMod](https://www.sourcemod.net/about.php) [datamaps](https://drive.google.com/drive/folders/12x4noWQ3YFAyv-TDUPzOyh8cq1z1yOYU?usp=sharing). Many outdated settings have also been removed. I also added/redid material exclusion (less clutter in the texture browser) and new visgroup categories.

Remember you can view all of the information in an FGD at any time by clicking the Help button inside Hammer.

![image](https://user-images.githubusercontent.com/39359267/120943117-9474cd00-c6f2-11eb-81eb-7c82ee4adb80.png)

![image](https://user-images.githubusercontent.com/39359267/120943126-a48cac80-c6f2-11eb-85bd-13a209c362a7.png)


# What's changed?
All of it... but to be more specific, here's the new and removed entities for each game:

* **Counter-Strike: Source**: Removed 82 bad entities, added 22 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/138302217-536b017d-c94f-4cfc-afe0-d0340dbbe64b.png)
* **Counter-Strike: Global Offensive**: Removed 110 bad entities, added 72 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/138299789-28d0024f-2795-48d0-bdb9-57d907f24e54.png)
* **Portal 2**: Removed 142 bad entities, added 24 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/121007390-9b81f680-c757-11eb-9ef4-5a202b30f736.png)
* **Left 4 Dead 2**: Removed 91 bad entities, added 18 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/138311431-3cd4b181-c572-4ce8-a52c-476daa8b2635.png)
* **Half-Life 2**: Removed 55 bad entities, added 20 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/138314738-82b8a20a-240c-4a2e-9aeb-173cab01b4af.png)


And, here are some examples of changed descriptions:

**StartFogTransition (env_fog_controller)**

Original|New
--|--
"*Start fog transition.*" | "*When fired, the fog fades to any new values sent through the 'LerpTo' inputs. Fade time is determined by the Interpolate time keyvalue.*"

**npc_hunter_maker from Half-Life 2**

Original|New
--|--
"*An entity that creates hunters. The NPCs it creates are clones of a template NPC.*" | "*It makes a clone of a hunter that's placed inside Hammer, and copies all of its properties and outputs. When using the SpawnMultiple input, any hunters in the map without an entity to follow (probably a strider) will have their name set to the name of this maker's template hunter so that when the FollowStrider input fires from map logic, they'll guard the new strider. (Renamed hunters will automatically move to where the npc_hunter_maker is, not the strider.) This entity is used in the Episode Two chapter Our Mutual Fiend.*"

**info_survivor_rescue from Left 4 Dead 2**

Original|New
--|--
"*Survivor rescue point*" | "*When a survivor dies, they will respawn here and can be rescued by living survivors who open the prop_door_rotating closest to this entity. Usually these doors open to closet-size rooms which serve no other purpose. Exactly three should be put in each rescue room.*"

**Should auto aim (env_portal_laser from Portal 2)**

Original|New
--|--
"*Default to enabled*" | "*Allows the laser to bend itself slightly to reach a prop_laser_catcher or point_laser_target. Does not apply if the beam has gone through a reflector cube.*"

**prop_mapplaced_long_use_entity from CS:GO**

Original|New
--|--
"*A map placed entity which activates with long use.*" | "*It's an object that requires a player to continuously press +use on it to interact with it.*"

# Legacy support entities
Entities (e.g. func_wall) that are meant to be replaced with other entities have been moved to their own FGD files and are still usable.

# Issues
If you think I should change something, you can tell me that.
