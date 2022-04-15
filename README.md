# BS2 Changelist

> **Note:** This file need to be expanded upon - the information listed below is a limited representation of the actual changes that have taken place. It's best to dive in and take a look for yourself, ask the writers of particular files any questions you have about them. And most importantly, please forward any opinions you have to them - be it positive, negative, whatever.

## Major Changes

- The 'Rules System' has been renamed to the 'Functions System', and is now present in `settings.yml`.
  - The Functions System is a complete redesign of the Rules System which is easier to use, and much more powerful.
- A new file, 'Advanced Settings' (in `advanced.yml`) has now replaced the old `settings.yml` (which only really had advanced settings in it anyways).
- 'Inclusive lists' and 'exclusive lists' have been renamed to more understandable counterparts: 'is in list' and 'is not in list' respectively.
- A new translation system has replaced `messages.yml`. Much more is translatable, and translations are easier to write, copy, etc.

## Changes since `bs0`

- Just about everything
- 'Buffs' are a new name for the attribute multiplier system
- Buffed attributes can only be targeted as inclusive lists now. This is intentional for safety reasons
- Buff's attribute multipliers are by default limited to at least `1.0` regardless of the formula used. This can be unlocked by specifying a different minimum boundary for a specific buff.

## Changes since `bs1`

- Refactored almost everything in the settings.yml file.
- Event 'on-player-teleport' is now triggered by 'on-player-change-world' as well. Function Events will not exactly match their Bukkit counterparts.
