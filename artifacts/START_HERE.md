# Dwarf fixes without the Thunderer reload merge

[Download DWARF_FIXES_NO_THUNDERER_MERGE.pack](DWARF_FIXES_NO_THUNDERER_MERGE.pack)

This is an import pack for your existing compatibility pack. It restores the
supplied original dwf_axe_shield_fix.animpack byte-for-byte. This is the ONLY
file in the pack. It contains animation database fragments, with no loose clips
or metadata assets. The other nine animation sets stay exactly as supplied. The original, unmerged rifle set is preserved
because an existing mercenary unit also uses its name; no failed Thunderer
reload merge is retained.

There are no DB files, no @marthreload.animpack, no animation or ramrod assets, and
no unit assignment edits in this import. Keep your working assignments for the
other units. Original Reloading Animations and texture/model fixes stay enabled.

## Import and remove the previous Thunderer patch

1. Back up your compatibility pack, then import ALL contents of this pack into
   it and allow replacement of dwf_axe_shield_fix.animpack. Keep that newly
   restored file; do not delete it after importing.
2. If the previous Thunderer patch has not already been removed, delete ONLY
   these four files from your compatibility pack (never from the original mods):

   ```text
   animations/database/battle/bin/@marthreload.animpack
   db/battle_animations_table_tables/!!!!awd_thunderer_reload_registration
   db/culture_to_battle_animation_tables_tables/!!!!awd_thunderer_reload_registration
   db/land_units_tables/!!!!!!!awd_thunderer_reload_charge
   ```

3. Keep the standard Thunderer row wh_main_dwf_inf_thunderers_0 assigned to
   hu3_dwarf_axe_shield_rifle in BOTH existing land_units_tables files:
   !!!!!laf_dwarfs_vanilla_units and !!!awd_vanilla_plus_expanded.
   Leave all other rows, stats and animation assignments as they are.
4. Save. Keep the two original mods enabled and any earlier diagnostic packs
   disabled as separate launcher mods.

If you already completed the rollback, only step 1 is needed.
Importing files cannot delete stale files, which is why step 2 is separate.
Older loose reload/ramrod copies from the imports match the original reload
mod's assets and do not contain the failed animation-table merge.

The source animation database container is preserved byte-for-byte. All clips,
metadata, skeletons and models are supplied by your existing enabled mods.
This package restores the working non-Thunderer setup reported by you; the
assistant has not tested playback in Warhammer III.

SHA-256: eb46db6207ae1e1d07639eac4a30892859ab5657d57f09e98b2add609c9837d3

Previous Thunderer patch files are historical failed attempts; use the import linked above.
