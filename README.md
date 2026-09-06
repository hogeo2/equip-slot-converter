# Equip Slot Converter

A free tool for **Monster Hunter Wilds** that converts Ver.R-based armor mods (and similar layered/replacer mods) to a different equipment slot — so a mod built for one armor piece can be worn in another slot, with meshes, textures, and physics carried over automatically.

🆓 **Free forever.** No paywall, no locked tiers, no catch.

## What it does

- Rebuilds the equip prefab from a vanilla donor for the target slot
- Renames mesh / mdf2 / chain2 / clsp files to match the new slot
- Rewrites texture paths
- Retunes bust-jiggle physics (optional — can be skipped)
- Handles both single mods and grouped, multi-variant releases automatically
- Output matches whatever format you fed in — `.zip` in gives `.zip` out, `.rar` in gives `.rar` out, folder in gives folder out
- Built for **hunter armor only** (Male/Female player slots) — it does not support Handler, Palico, or other NPC equipment; those use an entirely different character model system

## Before you start

This tool assumes you already have a working modding setup:

- **Blender 4.5**, with [RE-Mesh-Editor](https://github.com/NSACloud/RE-Mesh-Editor), [RE-Chain-Editor](https://github.com/NSACloud/RE-Chain-Editor) and [RE-Asset-Library](https://github.com/NSACloud/RE-Asset-Library) installed and enabled
- Game files extracted through RE Asset Library (Model Related Files, Prefab Files, User Files)
- 7-Zip and/or WinRAR, if your source mod is a `.zip`/`.7z`/`.rar` archive

Full setup and usage instructions are included in **How to Use.html** inside the download.

⚠️ Because of this environment requirement, support for individual setup issues is limited — please make sure your Blender/RE-tools environment is working correctly before reaching out. For questions or bugs, please use [GitHub Issues](../../issues) rather than DMs.

If Blender crashes or the log stops partway through a run, just click **Run Conversion** again — this can happen occasionally, usually on one specific file. It's safe to retry: the tool never touches your original mod, and always writes to a fresh output folder, so a failed run leaves nothing behind to clean up.

## Download

Grab the latest release from the [Releases page](../../releases/latest) — it's a single zip containing the tool, the usage guide, and license notices.

Only the compiled `.exe` is distributed here; this repository does not include the tool's source.

## Please respect mod authors

This tool converts a mod's equipment slot for **your own personal use**. Redistributing someone else's mod — converted or not — without the original author's permission is not okay. If you share a conversion, keep it to yourself or ask the original author first.

## Support

If this tool saved you time, a coffee is always appreciated — but it's free forever either way. 🙏
[ko-fi.com/pogeo](https://ko-fi.com/pogeo)

## Verifying your download

Each release's notes include a SHA-256 checksum for the release zip. To verify the file you downloaded matches:

```powershell
Get-FileHash "EquipSlotConverter-v1.0.2.zip" -Algorithm SHA256
```

## Disclaimer

This tool is distributed as a compiled `.exe`. Only download it from this repository's [Releases page](../../releases/latest), and verify the SHA-256 checksum before running it. Beyond that, it's provided as-is, with no warranty — use it at your own risk. The author isn't responsible for pre-existing issues on your device (a system that was already compromised, infected, or misconfigured before running this tool), for anything your own antivirus/security software should be handling, or for any damage to your mods, save data, or game installation.

This tool doesn't request admin rights, doesn't touch anything outside your chosen mod folders and its own settings file, and doesn't connect to the network except when you click the Ko-fi link yourself. It never modifies your original mod files — it always writes its output to a new folder and stops if that folder already exists. Still, it rebuilds and rewrites binary game files, so mistakes are possible: keep a backup of your Mods folder, and test a converted result in-game before assuming it's correct.
