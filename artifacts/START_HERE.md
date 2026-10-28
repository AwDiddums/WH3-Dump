# THUNDERER_PATCH.pack: minimal import

[Download THUNDERER_PATCH.pack](THUNDERER_PATCH.pack)

This import contains exactly FOUR files. Reloading Animations and the original
texture/model fixes must both remain enabled to provide the existing assets.
No loose animation, skeleton or model assets are duplicated here.

## Install

1. Back up your FULL compatibility pack.
2. In RPFM import ALL FOUR files from THUNDERER_PATCH.pack into that pack and
   replace matching files. Save your full pack.
3. If you imported a modified `@marthreload.animpack` from an earlier diagnostic,
   remove `animations/database/battle/bin/@marthreload.animpack` ONLY from your
   compatibility pack. Leave the original Reloading Animations mod untouched.
   Omitting this file from a new import does not delete an older copy.
4. Keep the two original mods and your patched compatibility pack enabled.
   Earlier diagnostic/import packs must not be enabled separately.

The four files are:

```
animations/database/battle/bin/dwf_axe_shield_fix.animpack
db/battle_animations_table_tables/!!!!awd_thunderer_reload_registration
db/culture_to_battle_animation_tables_tables/!!!!awd_thunderer_reload_registration
db/land_units_tables/!!!!!!!awd_thunderer_reload_charge
```

The animpack retains all ten fragments. Its combined rifle set uses
`dwf_axe_shield_rifle_fix`. The single unit row restores this assignment for
standard Thunderers using the stats from the supplied export. No other unit
table files or assignments are replaced.

All retained file contents are byte-identical to the CLEAN_REBUILD package.
This trim changes packaging and dependencies only; it is not a new animation
revision or an in-game-verified fix. The original playback problem remains
unconfirmed. Earlier failed versions are historical records, not additional
installation steps. Do not delete whole folders from your full compatibility
pack, since they may contain unrelated assets.

SHA-256: `f26432e55a1e8ff669e46342357e9938e00cb2494d494af7d1fc72c703af11fc`
