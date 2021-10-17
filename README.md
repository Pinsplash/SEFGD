Update: Hi, I haven't updated this in a while but I am still working on it slowly. I will be updating in a few days.
This is a collection of brand new [FGD](https://developer.valvesoftware.com/wiki/FGD) files for Source engine games. FGD files tell Hammer what entities there are, and what settings, inputs, and outputs they have.

Most of the information in these files was rewritten from scratch by me to be more accurate, comprehensive, and easier to follow. A lot of things I've written in them are confirmed by in-game testing and checking code. New entities, flags, keyvalues, inputs and outputs were found by referring to [dumpentityfactories](https://developer.valvesoftware.com/wiki/Dumpentityfactories), [code resources](https://github.com/ValveSoftware/source-sdk-2013/) in many places on the internet, [Source.Python](http://wiki.sourcepython.com/), and [SourceMod](https://www.sourcemod.net/about.php) [datamaps](https://drive.google.com/drive/folders/12x4noWQ3YFAyv-TDUPzOyh8cq1z1yOYU?usp=sharing). Many outdated settings have also been removed. I also added/redid material exclusion (less clutter in the texture browser) and new visgroup categories.

Remember you can view all of the information in an FGD at any time by clicking the Help button inside Hammer.

![image](https://user-images.githubusercontent.com/39359267/120943117-9474cd00-c6f2-11eb-81eb-7c82ee4adb80.png)

![image](https://user-images.githubusercontent.com/39359267/120943126-a48cac80-c6f2-11eb-85bd-13a209c362a7.png)


# What's changed?
All of it... but to be more specific, here's the new and removed entities for each game (slightly out of date):

* **Counter-Strike: Source**: Removed 83 bad entities, added 20 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/121004992-f0703d80-c754-11eb-8d35-1a8532c4dfc4.png)
* **Counter-Strike: Global Offensive**: Removed 108 bad entities, added 70 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/121006492-92445a00-c756-11eb-9bbc-354011960686.png)
* **Portal 2**: Removed 146 bad entities, added 23 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/121007390-9b81f680-c757-11eb-9ef4-5a202b30f736.png)
* **Left 4 Dead 2**: Removed 92 bad entities, added 17 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/121008617-cd478d00-c758-11eb-9a11-1f14aa389d9e.png)
* **Half-Life 2**: Removed 57 bad entities, added 20 new ones. [[Image]](https://user-images.githubusercontent.com/39359267/121017347-cd4c8a80-c762-11eb-952d-b399ad4b3777.png)

And, here are some examples of changed descriptions:

**StartFogTransition (env_fog_controller)**

Original|Mine
--|--
"*Start fog transition.*" | "*When fired, the fog fades to any new values sent through the 'LerpTo' inputs. Fade time is determined by the Interpolate time keyvalue.*"

**npc_hunter_maker (Half-Life 2)**

Original|Mine
--|--
"*An entity that creates hunters. The NPCs it creates are clones of a template NPC.*" | "*It makes a clone of a hunter that's placed inside Hammer, and copies all of its properties and outputs. When using the SpawnMultiple input, any hunters in the map without an entity to follow (probably a strider) will have their name set to the name of this maker's template hunter so that when the FollowStrider input fires from map logic, they'll guard the new strider. (Renamed hunters will automatically move to where the npc_hunter_maker is, not the strider.) This entity is used in the Episode Two chapter Our Mutual Fiend.*"

**info_survivor_rescue (Left 4 Dead 2)**

Original|Mine
--|--
"*Survivor rescue point*" | "*When a survivor dies, they will respawn here and can be rescued by living survivors who open the prop_door_rotating closest to this entity. Usually these doors open to closet-size rooms which serve no other purpose. Exactly three should be put in each rescue room.*"

**Should auto aim (env_portal_laser) (Portal 2)**

Original|Mine
--|--
"*Default to enabled*" | "*Allows the laser to bend itself slightly to reach a prop_laser_catcher or point_laser_target. Does not apply if the beam has gone through a reflector cube.*"

**prop_mapplaced_long_use_entity (CS:GO)**

Original|Mine
--|--
"*A map placed entity which activates with long use.*" | "*It's an object that requires a player to continuously press +use on it to interact with it.*"

# Legacy support entities
Some entities (e.g. func_wall) that are meant to be replaced with other entities are included in these FGDs for basic legacy support. They are noted as obsolete and have the obsolete sprite, and are included in the "removed" counts above. (This will soon change.)

# Issues
If you think I should change something, you can tell me that.
