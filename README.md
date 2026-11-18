# PS1 and PS2 Classics Package Studio

Create PS3 Classics packages from supported **PS1 and PS2 disc images** on Windows.

## Download

Download the **Windows ZIP** from [Releases](../../releases/latest), extract it, and run `PS1 and PS2 Classics Package Studio.exe`. The release also includes a source archive and third-party notices.

The Windows app includes its runtime and the pop-fe PS1 engine, so Python is not required for the bundled PS1 workflow. The PS2 toolkit workflow requires the separately obtained and extracted [PS2 Classics GUI toolkit](https://www.psx-place.com/resources/ps2-classics-gui.638/) or a compatible external engine.

## Features

- Create packages from PS1 CUE/BIN images and PS2 DVD ISOs, with automatic system detection where possible.
- Queue multiple games and create separate packages one at a time.
- Look up PS1 and PS2 cover artwork before a build and see whether a match was found. Manual icon and background selection are also available. Automatic PS2 cover lookup requires the PS2 Classics GUI toolkit.
- Choose PS1 emulator compatibility options and use available PS2 compatibility profiles.
- Watch build activity and cancel when needed; supported PS2 toolkit builds show estimated progress.
- Optionally try a PS2 widescreen patch matched to the game's serial and boot executable checksum.

Cover lookups access the internet using the disc ID. The PS1 engine may also retrieve artwork, manuals, or audio online. Covers come from the [PS1](https://github.com/xlenore/psx-covers) and [PS2](https://github.com/xlenore/ps2-covers) collections.

### PS2 widescreen

The bundled [PCSX2 community patch database](https://github.com/PCSX2/pcsx2_patches) provides experimental static patches for supported games. The app reports whether a patch was applied or skipped. Some patches require runtime behavior and may not work with this approach. This option uses the toolkit engine and is not applied to pop-fe2 multi-disc builds.

## Requirements and compatibility

A compatible PS3 setup, such as HEN or CFW configured for homebrew packages, is required. PS2 toolkit builds also require the placeholder license matching the toolkit template. Package creation and artwork lookup have been tested, but PS3 playback of this version has not been verified. Game compatibility varies. Original disc images remain unchanged.

## Credits

PlayStation and PS1/PS2 Classics are products of Sony. PS2 Classics GUI is by Aldo Vargas (aldostools); ps2classic is by the ps3dev-net team; pop-fe and pop-fe2 are by Ronnie Sahlberg and contributors. Thanks to Jabu for the PS2-FPKG workflow reference, the PSL1GHT Development Team, Hykem and contributors, the ManaGunZ contributors, PCSX2 patch authors, and the artwork collections' contributors. Additional notices for bundled helpers are included in the release. The [pop-fe project](https://github.com/sahlberg/pop-fe) provides its source and third-party information.
