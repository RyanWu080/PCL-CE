 [绠€浣撲腑鏂嘳(README.md) | **English** | [绻侀珨涓枃](README-ZH_TW.md)

# PCL-CE unrestrict

An unofficial fork that follows [PCL-CE](https://github.com/PCL-Community/PCL-CE) releases and builds Windows executables with region-based feature restrictions disabled. The patch changes `RestrictedFeaturePolicy.cs` while retaining region assessment.

## Downloads

Open [Releases](https://github.com/RyanWu080/PCL-CE-unrestrict/releases) and download an executable ending in `_unrestrict.exe`: x64 for Intel/AMD PCs, ARM64 for Windows on ARM. Install [.NET 10 Desktop Runtime](https://get.dot.net/10).

GitHub's source archives refer to the original upstream tags. The applied patch is stored in `.github/release-sync/RestrictedFeaturePolicy.cs`; `unrestrict-build.json` records the source and binary checksums.

## Release tracking

- Starts at **v2.15.1 stable**. Older versions and v2.15.1 betas are excluded; later stable and beta versions are included.
- Checks upstream releases hourly at minute 41. GitHub scheduling may be delayed.
- Builds x64 and ARM64 from each exact official tag with the guarded patch. Publishes only after successful builds.
- Copies the official tag, title, description and prerelease status. Executable filenames include `unrestrict`; published binaries are not repeatedly rebuilt. Description changes are synchronized.
- Stops if the policy changes, the patch is incompatible or compilation fails.

Release descriptions are copied verbatim. External download links and signing information in those descriptions refer to the official binaries, not the modified assets here.

## Repository layout

`dev` holds this fork's documentation and automation. `custom/dev-unrestricted` merges upstream development code hourly at minute 23, preserving a dedicated patch commit and stopping on conflicts without force-pushing; its documentation remains upstream's. Release builds use official tags independently of this development branch.

The workflows are `sync-custom-dev.yml` and `follow-official-releases.yml`. Builds run without official private service credentials, separately from the job that publishes assets.

## Validation and attribution

Automation, filtering, compilation and publishing have been verified. Startup, login and download features still require runtime testing. Features requiring official private service credentials may differ from official builds. Upstream signatures do not apply to modified binaries.

Source: [PCL-Community/PCL-CE](https://github.com/PCL-Community/PCL-CE), maintained by community developers and based on PCL by 榫欒吘鐚穬. `Plain Craft Launcher 2/` retains its [custom license](Plain%20Craft%20Launcher%202/LICENCE); other directories retain [Apache License 2.0](LICENSE). Original licenses, copyright and attribution are preserved.

Investigate fork-specific automation and patch issues here before reporting them as official-release issues.
