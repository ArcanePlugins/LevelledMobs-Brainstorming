# What's changed in LM4?

- This is just a brief summary of what we've done in LM4. Many minor details are missed!

## Highlights

- Full re-write of the entire plugin - this was a ton of work!
- Whole configuration system has been refined and is far easier to use.
  - All LM3 configs except for Custom Drops **cannot** be migrated automatically by LM.
- To your players, LM4 will look exactly the same as LM3, and this is intended - players are enjoying LevelledMobs as-is. We wanted to take the extra step to make server owners and developers even happier. :)

## Configuration Changes

### Settings and Rules

- We've created **Simple Settings**, an area in `settings.yml` which makes it so much easier for newbies to make the simple configuration changes (which most users want anyways) without having to touch any of the Rules System whatsoever.
  - You can change what worlds mobs can be levelled in, their difficulty, and various other simple changes which most users are satisfied with.
- We've refined the Rules System to make it more powerful and easier to use.
- The way the Rules System works in LM4 is so different internally that we unfortunately can't automatically migrate your LM3 rules.
- We've moved Presets into `presets.yml` to declutter the file - same with mob groups and biome groups into `groups.yml`.
- Additionally, groups in `groups.yml` don't have to be for entities or biomes anymore, groups can hold anything in them.
- Lastly, a handful of presets and groups supplied by LevelledMobs (especially the challenge presets) are now inbuilt instead of cluttering your file.
  - This is so you can always have the latest updates and tweaks to them.
  - You can override the inbuilt ones by creating a group or preset under the same name, and LM will use the one you provide instead. Or, create a group or preset with a different name and use that instead.

### Custom Drops Changes

- We didn't have many changes to make to Custom Drops as it was designed pretty well from the get-go; a handful of simple refinements were made to keep it as polished as possible. It functions almost identically to LM3's implementation on the outset, though things are handled quite differently inside the plugin's code.
- Your old custom drops can be migrated across automatically, zero-effort. Woot!

### Translations Changes

- LM now ships with a handful of popular translations in-built:
  - English (USA) (`en_US`)
  - German (`de_DE`)
  - Spanish (`es_ES`)
  - French (`fr_FR`)
  - English (Australia) (`en_AU`)

## Codebase Changes

- The plugin's source code has been **completely** written from the ground up in Kotlin.

- This achieves:
  - Full compatibility with Folia.
  - More performant code utilising more multithreading.
  - A proper API decoupled from the plugin's code, far better for developers to use.
  - Cleaner, organised code, making it easier for maintainers and contributors to work on.
  - Internal code is also written in a way which third-party 'addons' can be created for LM easily.
  - Future-proofing.
