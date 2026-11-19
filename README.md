# PS3 Package Studio

Create PS3 Classics packages from supported **PS1 and PS2 disc images** on Windows. The standalone studio includes its standard PS1 and PS2 engines, desktop runtime, disc-identification data, and packaging resources.

**[Download the latest Windows ZIP](https://github.com/Laudadio93/ps2-classics-package-studio/releases/latest)**, extract it, and open **PS3 Package Studio.exe**. A separate Python installation or packaging application is not needed for the built-in workflows.

## What's new

- **PS3 Package Studio** is available as a standalone app with the new electric-blue PS3 and package Windows icon.
- PS1 and PS2 manual previews are handled on the PC. Missing, corrupt, or still-downloading manuals do not block package creation.
- The built-in PS1 engine is prevented from picking up manuals beside the disc or from its catalog. The PS2 builder omits the former console-manual writing step.
- For compatible external engines, the studio checks the staged package for recognized console manual entries and rebuilds the package when necessary before delivery.
- Final PS3 PKG writing is accelerated for recognized bundled runtimes. Custom engines retain their own writer.
- The current release includes the PS1 and PS2 features, offline data, artwork tools, compatibility settings, queue, progress display, and visual refinements from the combined studio.

## Create packages

1. Select a supported PS1 or PS2 disc image. Keep PS1 CUE files and their referenced tracks together.
2. Review the detected system, title, game ID, and status indicators. Add additional games to build them one at a time, or select multi-disc mode for a supported engine.
3. Review artwork, compatibility settings, and any optional patches. Choose an output folder with enough room for temporary files and finished packages.
4. Start the build. Follow the activity log, percentage and estimated time where available. The completion message shows the output location.

The Windows build includes the standard engines. The interface also supports a user-selected compatible pop-fe or pop-fe2 engine.

## PS1 support

- Import supported **CUE, BIN, IMG, and CCD** images, subject to engine support.
- Build separate packages in a sequential queue or use supported multi-disc mode for up to five discs, with optional in-game disc swapping.
- See disc, PS1 audio, artwork, and manual indicators. Hover for their status explanations.
- Consult the bundled LibCrypt index and select an alternate PS1 emulator when appropriate. An unlisted or unreadable ID does not prove a disc is unprotected.
- Apply a custom **.ps3config** to one CUE disc. For a single-disc, single-BIN CUE, apply supported PPF2, PPF3, or xdelta patches to a working copy. Match the patch to the game revision.
- SBI files can be detected, but the bundled engine does not import them. Patch and configuration options depend on the selected engine and disc layout.

## PS2 support

- Build a PS2 DVD ISO as a PS3 Classics package. The built-in PS2 engine processes one DVD ISO per package. A queue creates separate packages sequentially.
- Use automatic compatibility profiles, select a specific profile, disable it, supply a custom CONFIG, or generate an advanced configuration using the available cache, performance, pressure-button, and multitap controls.
- Match supported widescreen patches by game serial and boot-executable checksum. Availability depends on the title and revision.
- Open community compatibility reports for manual review. Profiles and patches do not guarantee compatibility on a console.

## Disc checks, artwork, and manuals

- **Offline disc verification** compares supported images with bundled Redump SHA-1 records. The PS2 check supports single-file DVD ISOs. The PS1 multi-track check expects one BIN per track, one INDEX 01 at 00:00:00 per track, and no gap directives. PS2 CD images, CHD images, and merged multi-track BINs are outside this check.
- **Status indicators** show whether the disc, referenced PS1 tracks, artwork, and manual were found. Track checks do not test audio playback.
- **Artwork** can be found before building, previewed, and cached. Choose standard or 3D covers where available, or select a custom icon and background. The PS3 menu preview is illustrative.
- **Menu audio** options depend on the engine and build mode. Supported engines offer automatic sound, silence, or a custom WAV.
- **Manual preview** opens supported PDFs and ZIP/CBZ page-image archives on the PC. PS1 lookup checks nearby files. PS2 lookup checks nearby files and the local library, and can optionally search the indexed online collection. Availability varies by title and region.
- **Online access** is optional for cover and manual lookup and community compatibility reports. Cached artwork and manuals can be reused offline.

The package builder excludes recognized console manual files. A missing or unreadable PC manual does not prevent a build.

## Build activity and output

The activity panel reports applicable copy, encryption, configuration, and package-writing stages. Progress, estimated time, cancellation, errors, and the completed output location are shown when supported. Rebuilding a package to remove recognized external-engine manual entries can require additional time and working space.

A Redump match identifies a known disc dump. A mismatch can reflect a different region, revision, modified image, or missing catalog entry. Console compatibility depends on the game, configuration, and PS3 environment.

## Credits and notices

- **Ronnie Sahlberg and contributors** developed [pop-fe](https://github.com/sahlberg/pop-fe) and [pop-fe2](https://github.com/sahlberg/pop-fe2), including PS1 packaging and PS2 manual references.
- **Aldo Vargas** created [PS2 Classics GUI](https://www.psx-place.com/resources/ps2-classics-gui.638/). The **ps3dev-net team** developed ps2classic.
- **PSL1GHT Development Team**, **Hykem and contributors**, and **OpenSSL contributors** provided package-writing, make_npdata, and cryptographic components. [PSL1GHT](https://github.com/ps3dev/PSL1GHT) · [OpenSSL](https://openssl.org/)
- **PCSX2 patch authors**, **ManaGunZ contributors**, and **Jabu** provided patch, compatibility, and PS2-FPKG workflow references. [PCSX2 patches](https://github.com/PCSX2/pcsx2_patches) · [ManaGunZ](https://github.com/Zarh/ManaGunZ) · [PS2-FPKG](https://www.psx-place.com/resources/ps2-fpkg.1628/)
- **Redump contributors** and **tsitokely** provided disc-identification data. [Redump](https://redump.org/) · [ps2-iso-renamer](https://github.com/tsitokely/ps2-iso-renamer)
- **xlenore and contributors** organize cover artwork. **Kirkland's Manual Labor** and the **Internet Archive** preserve and host manuals. [PS1 covers](https://github.com/xlenore/psx-covers) · [PS2 covers](https://github.com/xlenore/ps2-covers) · [PS2 manuals](https://archive.org/details/kirklands-manual-labor-sony-playstation-2-usa-4k-version)
- **PDFium contributors**, **Joshua MacDonald and xdelta contributors**, and **ps3classics/ps2 and PS3 Developer Wiki contributors** provide rendering, patch, and configuration tools and references. [PDFium](https://pdfium.googlesource.com/pdfium/) · [xdelta](https://github.com/jmacd/xdelta) · [PS2 CONFIG guide](https://github.com/ps3classics/ps2)
- **Laudadio93** maintains the application. PlayStation systems, software, and marks belong to Sony Interactive Entertainment and their respective owners.

The application carries a PS3 placeholder activation file. Redistribution rights for that file have not been confirmed.

Earlier versions and their original release notes remain in the [release history](https://github.com/Laudadio93/ps2-classics-package-studio/releases).
