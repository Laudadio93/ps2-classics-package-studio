# PS2 Classics Package Studio

Build PS3 PS2 Classics packages from PS2 DVD ISOs on Windows.

## Download

Download the **Windows ZIP** from [Releases](../../releases/latest), extract it, and run `PS2 Classics Package Studio.exe`. The release also includes a source archive.

The Windows executable includes its runtime. The standard packaging workflow additionally requires the separately obtained and extracted [PS2 Classics GUI toolkit](https://www.psx-place.com/resources/ps2-classics-gui.638/), including its encryption tools and template. Python is not required for this workflow.

## Features

- Queue multiple games and create separate packages one at a time.
- Watch the current build stage and estimated progress; cancel when needed.
- Use the optional pop-fe2 command-line engine for multi-disc packages and XMB audio.
- Optionally try a widescreen patch matched to the game's serial and boot executable checksum.

### Widescreen

The bundled [PCSX2 community patch database](https://github.com/PCSX2/pcsx2_patches) provides experimental static patches for supported games. The app reports when a patch is applied or skipped. Some patches require runtime behavior and may not work with this approach. This option uses the toolkit engine and is not applied to pop-fe2 multi-disc builds.

## Requirements and compatibility

A PS3 configured for PS2 Classics and homebrew packages, such as HEN or CFW, and the placeholder license matching the toolkit template are required. The app checks the output package structure, but playback and game compatibility must be verified on the PS3. The original ISO remains unchanged.

Read the included guide for setup, output storage, and details.

## Credits

PlayStation and PS2 Classics are products of Sony. PS2 Classics GUI is by Aldo Vargas (aldostools); ps2classic is by the ps3dev-net team; pop-fe2 is by Ronnie Sahlberg and contributors. Thanks to Jabu for the PS2-FPKG workflow reference, the PSL1GHT Development Team, Hykem and contributors, the ManaGunZ contributors, and PCSX2 patch authors. Additional notices and source for bundled helpers are in `ThirdParty.zip`.
