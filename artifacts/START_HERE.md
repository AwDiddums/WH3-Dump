# Use only THUNDERER_PATCH.pack

[Download THUNDERER_PATCH.pack](THUNDERER_PATCH.pack)

This is the consolidated Thunderer rebuild under one simple filename. Its
contents are byte-identical to the previous CLEAN_REBUILD import, not a newly
verified solution. Game playback is still unverified. Earlier versions failed
in the user's tests; they must not be represented as confirmed fixes.

## Install

1. Back up your FULL compatibility pack.
2. In RPFM, import ALL contents of THUNDERER_PATCH.pack into that pack and allow
   matching files to be replaced. Save your full pack.
3. Keep Reloading Animations, the original texture/model fixes, and your patched
   compatibility pack enabled. Disable any older diagnostic/import packs if
   enabled separately in the launcher. They are historical versions only.

Do not replace your whole compatibility .pack file with this small import pack.
No manual Man Animation edits are required. The included one-row table selects
`dwf_axe_shield_rifle_fix` for standard Thunderers, retaining their exported stats.
All other unit table files and assignments remain untouched.

The package restores original `@marthreload.animpack` bytes to reset diagnostic
copies, installs the combined custom rifle set, includes reload/charge assets,
and adds the rifle registration/culture link. Other custom fragments are
preserved. It does not add crossbow reload animations.

Only basic Thunderers are the intended repair target: reload plus melee charge
attacks. The runtime cause has not been conclusively identified; an in-game
check of this consolidated state is still needed.

## Historical files

All other import/test pack names in this directory are superseded. Use none of
them in addition to this package. They are retained as records, not additional
installation steps.

SHA-256: `165551af4daab719e8b9846bb6e93e7f25cc8bec9f8be7ea9de8eec3b207a139`
