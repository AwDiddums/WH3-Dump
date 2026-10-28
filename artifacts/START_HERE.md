# Restore original Thunderer reload setup

[Download THUNDERER_REVERT.pack](THUNDERER_REVERT.pack)

This reverses our basic-Thunderer edits. It does not merge charge attacks into
Thunderers. No animation clips, metadata assets, skeletons or models are included;
your existing enabled mods supply them.

## Import

Back up your compatibility pack. Import ALL SIX files from THUNDERER_REVERT.pack
into that same pack, allowing all matching files to be replaced. Save it.
Keep Reloading Animations and the original texture/model fixes enabled.
Keep old diagnostic packs disabled as separate launcher mods.

The import performs the rollback directly; no manual row deletion or assignment
editing is needed for the known files from your supplied export.

## Exact changes

- Restore animations/database/battle/bin/@marthreload.animpack byte-for-byte
  from your original marthreload.pack. This restores all five original fragments;
  the native Thunderer fragment has no inserted jumping attacks.
- In db/land_units_tables/!!!!!laf_dwarfs_vanilla_units and
  db/land_units_tables/!!!awd_vanilla_plus_expanded, change only
  wh_main_dwf_inf_thunderers_0 -> man_animation = hu3_dwarf_axe_shield_rifle.
- Replace our previous extra land-unit override and two registration tables with
  valid empty tables at their same paths, clearing the rows left by our patches:
  db/land_units_tables/!!!!!!!awd_thunderer_reload_charge
  db/battle_animations_table_tables/!!!!awd_thunderer_reload_registration
  db/culture_to_battle_animation_tables_tables/!!!!awd_thunderer_reload_registration

Every other unit row and stat is preserved byte-for-byte from the supplied
export. The melee-fix container is not included or changed, so the restored melee
sets for other units remain as they are. The three empty files contain no active
rows; leaving them empty is sufficient to clear their earlier contents.

The earlier DWARF_FIXES_NO_THUNDERER_MERGE.pack restored only the original melee
container. It contained no unit-table rollback. The earlier native-name test also
inserted five charge attacks; this rollback leaves the original reload container
completely unchanged.

Checks compare actual binary contents, source data and all other unit rows.
Game playback has not been verified by the assistant; this restores the original
source setup rather than claiming a verified fix for an unknown runtime conflict.

SHA-256: 8d13bf2b0d3631fdb3d610709426a4831bc8a83d4630222563d7f65bee840d5d

The separate melee restore import remains DWARF_FIXES_NO_THUNDERER_MERGE.pack.
