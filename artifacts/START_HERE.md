# THUNDERER_PATCH.pack — direct merge into the reload animpack

[Download THUNDERER_PATCH.pack](THUNDERER_PATCH.pack)

This package now merges the custom Thunderer rifle set INTO @marthreload.animpack.
It preserves all five original reload-mod fragments unchanged, adds the custom
rifle set with the supplied five melee fixes, and co-locates the supplied reload
and charge assets. The duplicate custom rifle is removed from the texture-fix
container; its nine other fragments stay byte-identical.

This is a structural change from the earlier fragments-only imports. It is NOT
an in-game-verified fix or proof that the earlier container layout caused the
failure. The screenshot suggested the co-located asset layout; the earlier
source upload had assets outside its animpack. No runtime claim is made.

## Install

1. Back up your full compatibility pack.
2. Import ALL FIVE files from THUNDERER_PATCH.pack into that pack, replacing
   matching files. Save your full pack. Do not replace the full pack itself.
3. KEEP BOTH included animation containers:
   - animations/database/battle/bin/@marthreload.animpack
   - animations/database/battle/bin/dwf_axe_shield_fix.animpack
   The earlier advice to remove a diagnostic @marthreload.animpack does not
   apply to this new merged container. This one contains the combined set.
4. Keep Reloading Animations and the original texture/model fixes enabled.
   Do not enable previous diagnostic/import packs separately.

The existing man_animation assignment stays dwf_axe_shield_rifle_fix.
The three small DB files are unchanged from the previous minimal package:
rifle registration, culture link, and the one standard-Thunderer unit row.
No existing unit table files are replaced. Other unit assignments and exported
stats remain unchanged. No loose asset folders need importing: the supplied
animation assets are inside the merged reload animpack. Original mods still
supply the ramrod model, vanilla audio and the other existing assets.

## Checks performed

- Decoded all377 pasted RPFM rows; five melee records match supplied fix exactly.
- All four reload entries match original source bytes.
- All five original reload fragments and all nine remaining fix fragments match.
- Exactly one custom rifle definition exists across the two delivered containers.
- All supplied reload and relevant charge clips/metadata are in the reload container.
- Wrapper indices, counts, DB records and round-trip reads pass.

Game playback remains unverified. Earlier packages remain historical records;
use this current file only.

SHA-256: `698787aa3da88096a67d199dbb95d171a7b78e16c6ea8567ac01c3b7df7c744c`
