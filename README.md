# Equip Slot Converter

A free tool for **Monster Hunter Wilds** that converts Ver.R-based armor mods (and similar layered/replacer mods) to a different equipment slot — so a mod built for one armor piece can be worn in another slot, with meshes, textures, and physics carried over automatically.

🆓 **Free forever.** No paywall, no locked tiers, no catch.

## What it does

- Rebuilds the equip prefab from a vanilla donor for the target slot
- Renames mesh / mdf2 / chain2 / clsp files to match the new slot
- Rewrites texture paths
- Retunes bust-jiggle physics (optional — can be skipped)
- Handles both single mods and grouped, multi-variant releases (DOTEI-style) automatically
- Output matches whatever format you fed in — `.zip` in gives `.zip` out, `.rar` in gives `.rar` out, folder in gives folder out

## Before you start

This tool assumes you already have a working modding setup:

- **Blender 4.5**, with [RE-Mesh-Editor](https://github.com/NSACloud/RE-Mesh-Editor), [RE-Chain-Editor](https://github.com/NSACloud/RE-Chain-Editor) and [RE-Asset-Library](https://github.com/NSACloud/RE-Asset-Library) installed and enabled
- Game files extracted through RE Asset Library (Model Related Files, Prefab Files, User Files)
- 7-Zip and/or WinRAR, if your source mod is a `.zip`/`.7z`/`.rar` archive

Full setup and usage instructions are included in **How to Use.html** inside the download.

⚠️ Because of this environment requirement, support for individual setup issues is limited — please make sure your Blender/RE-tools environment is working correctly before reaching out.

## Download

Grab the latest release from the [Releases page](../../releases/latest).

Only the compiled `.exe` is distributed here; this repository does not include the tool's source.

## Please respect mod authors

This tool converts a mod's equipment slot for **your own personal use**. Redistributing someone else's mod — converted or not — without the original author's permission is not okay. If you share a conversion, keep it to yourself or ask the original author first.

## Support

If this tool saved you time, a coffee is always appreciated — but it's free forever either way. 🙏
[ko-fi.com/pogeo](https://ko-fi.com/pogeo)

## Verifying your download

Each release includes a SHA-256 checksum in its notes. To verify the file you downloaded matches:

```powershell
Get-FileHash "Equip Slot Converter.exe" -Algorithm SHA256
```
