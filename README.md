# PS1 and PS2 Classics Package Studio

Create PlayStation 3 Classics packages from supported **PS1 and PS2 disc images** on Windows.

## Download

Download the [latest Windows ZIP](../../releases/latest), extract it, and run `PS1 and PS2 Classics Package Studio.exe`. The release also provides a source archive and third-party notices. The standard PS1 and PS2 workflows include their runtimes and engines; no Python installation or separate packaging application is required.

## Core features

- Automatically detect supported PS1 and PS2 disc images, queue multiple games, and build separate packages sequentially.
- Track build activity, progress and estimated time where supported, and cancel a build.
- Find and preview PS1 and PS2 cover artwork online or choose custom artwork; downloaded covers are cached.
- Use PS2 compatibility profiles, custom configurations, and optional matching widescreen patches.
- View detailed disc, audio, artwork and manual status before building.

For the exact supported formats, limitations and recent changes, read the release notes below and the README included in the download.

## PS1 and PS2 Classics Package Studio v0.7.0

This update adds a built-in PS2 packaging engine, offline disc verification, software manual support, PS1 patching and configuration options, and an illustrative PS3 menu preview. The standard PS1 and PS2 workflows run on Windows without a separate Python installation or companion application.

### What's new since v0.6.0

**Built-in PS2 engine**

- The standard PS2 Classics workflow now includes its engine, package writer, and supporting components inside the Windows executable. A separately downloaded PS2 Classics GUI toolkit is no longer needed for that workflow.
- The built-in PS2 engine creates one DVD ISO package at a time; a queue builds separate packages sequentially. External engines remain available for their supported workflows.
- Optional widescreen patches are matched to supported games; some patches require runtime behavior and cannot be applied by this workflow.

**Offline disc verification**

- An optional Verify disc button compares supported images with bundled Redump SHA-1 records and reports results in Build Activity. It shows progress and supports cancellation without changing the image.
- PS2 verification supports single-file DVD ISOs. The PS2 catalog snapshot is dated June 15, 2026.
- PS1 verification supports CUE files with one separate BIN per track, each with one INDEX 01 at 00:00:00 and no gap directives. All track hashes must match the same catalog entry. The PS1 snapshot is dated November 18, 2026.
- An unknown or unmatched image may be a different revision, modified, absent from the database, or damaged; a match does not guarantee game compatibility. Merged multi-track BINs, unsupported CUE layouts, PS2 CDs, and CHD files are not verified.

**Manuals**

- PS2 manuals can be selected as ZIP or CBZ archives of page images, detected beside the ISO, or located in a user-selected local library by game ID.
- If enabled and no local match exists, the app can look up supported U.S. PS2 game IDs in its included index, download a matching manual from Kirkland's Manual Labor collection, render and verify the PDF pages, and cache the result for later offline use. Coverage and availability are incomplete.
- Manual status is checked before building. Invalid selected manuals block the build; missing optional manuals do not. PS1 manual formats and their limitations are documented in the included README.
- PDF rendering uses bundled PDFium; no separate PDF application is required.

**PS1 options**

- A protection indicator reports whether the detected disc ID appears in the bundled pop-fe LibCrypt database. An unlisted or unreadable ID does not prove a disc is unprotected.
- Add a custom PS1 .ps3config for a single CUE disc. The engine appends its commands to its own configuration. Existing sidecar configs are also supported.
- Apply supported PPF2, PPF3, or xdelta patches to a single-disc, single-BIN PS1 CUE. The app copies the disc to a temporary working folder and leaves the original untouched. PPF variants require a matching validation block; xdelta uses its own patch validation. Extra disk space is needed.
- SBI files are detected but are not imported by the bundled engine. Patching queues, multi-disc packages, and multi-BIN CUEs is not yet supported.

**Compatibility and presentation**

- Offline PS2 profile lookup shows available profiles by disc ID, with automatic, specific, and custom CONFIG choices.
- Opt-in advanced PS2 CONFIG options expose documented cache, performance, pressure sensitivity, and multitap settings. They generate a new config instead of the automatic profile and do not guarantee a fix.
- A button opens community PS2 compatibility reports for manual review by title and region. The app does not yet automatically match those reports to individual disc IDs.
- Preview the PS3 menu with the chosen title, cover, background, and audio selection. This is an illustration; the console's actual presentation can differ.
- The activity area includes disc, PS1 disc-audio, artwork, and manual indicators with hover explanations. Artwork can be previewed, and downloaded covers can be reused from the local cache.
- About and third-party notices have been expanded to credit the referenced projects and data sources.

### Windows download

Download the **Windows ZIP**, extract it, and run `PS1 and PS2 Classics Package Studio.exe`. The executable contains the application runtime and the engines needed for the standard workflows. Internet access is optional for online artwork and manual lookup. The source archive is provided separately.

A compatible PS3 HEN or CFW setup and the appropriate PS2 Classics placeholder license are required. The release was tested on Windows, including Redump matches for PS1 Silent Hill and PS2 Dragon Ball Z: Budokai, synthetic verification and patch checks, and a PS1 package build using a custom config and patch. The new features have not been tested for gameplay on PS3 hardware.

### Credits

PS1 engine and PS2 manual references: [pop-fe / pop-fe2](https://github.com/sahlberg/pop-fe) by Ronnie Sahlberg and contributors. PS2 Classics GUI: Aldo Vargas; ps2classic: the ps3dev-net team. Disc catalog: [Redump](https://redump.org/) contributors; PS2 catalog snapshot sourced through [ps2-iso-renamer](https://github.com/tsitokely/ps2-iso-renamer), PS1 through [redump.info](https://redump.info/). Manuals: [Kirkland's Manual Labor](https://archive.org/details/kirklands-manual-labor-sony-playstation-2-usa-4k-version). PDF rendering: [PDFium](https://pdfium.googlesource.com/pdfium/). Delta patches: [xdelta3](https://github.com/jmacd/xdelta). Advanced CONFIG reference: [ps3classics/ps2](https://github.com/ps3classics/ps2) and PS3 Developer Wiki contributors. Thanks also to PCSX2 patch authors, ManaGunZ contributors, PSL1GHT, Hykem and contributors, and Jabu for the PS2-FPKG workflow reference. See included notices and licenses.

