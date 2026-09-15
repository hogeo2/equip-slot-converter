![Equip Slot Converter](https://github.com/user-attachments/assets/43a95a14-bc72-4b13-a6e5-509ca117fd09)

# Equip Slot Converter

A free tool for **Monster Hunter Wilds** that moves an armor mod to a different equipment slot — so a mod built for one armor piece can be worn in another, with meshes, textures and physics carried across automatically.

🆓 **Free forever.** No paywall, no locked tiers, no catch.

## What it does

- Rebuilds the equip prefab from a vanilla donor for the target slot
- Renames the mesh / mdf2 / chain2 / clsp files and rewrites every reference that pointed at them
- Carries the mod's own appearance parameters, physics and hairstyle-fitting data across
- Handles single mods, grouped multi-variant releases, and mods published as a `.pak` — it works out which kind it is on its own
- Output matches what you fed in: a `.zip` gives a `.zip`, a folder gives a folder
- Checks the result against the game's own data afterwards, and writes a report you can keep with the mod
- Adjusts body physics — bust, hips and thighs, each with its own numbers — on any mod folder, converted by this tool or not
- Repairs a mod built for an older game version
- Available in 8 languages; the run log deliberately stays English so it can be shared
- **Hunter armor only** (the Male/Female player equip slots). Handler, Palico and other NPC equipment use an entirely different character model system and are not supported.

## Requirements

- **Monster Hunter Wilds**, installed. The tool reads the game's own `.pak` files to build its copy of the game data, and only ever reads them — nothing under your game folder is written to or modified.
- About **600 MB** of free disk space for that extracted copy. Press **Set up** in the tool and it does the extraction for you; it shows the plan, and where it intends to write, before it starts.
- **7-Zip or WinRAR** — only if you want to convert a `.zip`/`.7z`/`.rar` mod archive directly. Mod folders and `.pak` files need neither.

**Blender is no longer required.** Earlier versions needed Blender 4.5 plus three RE add-ons; the tool now reads and writes the game's mesh, mdf2 and chain2 files itself, using a Python runtime bundled in the download. If you installed Blender only for this tool, you can remove it.

Full setup and usage instructions, with screenshots of every part of the window, are in **How to Use.html** inside the download.

## Download

Grab the latest release from the [Releases page](../../releases/latest). Unzip the folder somewhere you can write to — anywhere is fine — and double-click **Launch.bat**.

Keep the folder together: `Launch.bat` looks for `gui\` and `scripts\` next to itself. Your settings live in `settings.ps1` in that same folder and are never overwritten once created, so to update the tool, unzip the new version and copy your old `settings.ps1` across.

Nothing in the download is compiled or packed. It is a plain zip of PowerShell and Python scripts, so you can read every line of it before you run it.

## Reporting a problem

Please use [GitHub Issues](../../issues) rather than DMs. The useful report is the run log, plus which slot you converted **to** and **from**.

If a run stops partway through, just click **Run Conversion** again. It is safe to retry: the tool never touches your original mod, and always writes to a fresh output folder, so a failed run leaves nothing behind to clean up.

## Please respect mod authors

This tool moves someone else's armor mod to a different equip slot for **your own use**. That is not the same as redistributing the result. If you convert someone's mod and then share or re-upload it — on Nexus, Discord, anywhere — you are distributing a modified version of their work, and changing a mod's equip slot doesn't change who made it. Use this tool as much as you like for your own game; before sharing a converted mod with anyone else, ask the original author first.

## License

Released under the **GNU General Public License v3.0**. The full text is in `LICENSE` inside the download, and every source file carries the notice at its top.

It is GPL-3.0 because it has to be: the conversion engine reads and writes RE Engine binary formats using modules vendored from [RE-Asset-Library](https://github.com/NSACloud/RE-Asset-Library) and [RE-Mesh-Editor](https://github.com/NSACloud/RE-Mesh-Editor) by NSACloud, both GPL-3.0. Each vendored module ships with its full licence text and a provenance notice beside it.

In practice: use it for anything, including mods you release publicly — you owe no credit for a mod you converted with it, it's a tool. You may pass the tool itself on, modified or not, provided you keep the copyright and licence notices intact, state what you changed, and hand on the same GPL-3.0 terms together with the source.

No game data is included or redistributed. 7-Zip and WinRAR are separate programs under their own licences and are not part of this bundle. The bundled Python runtime and the third-party modules it carries are listed in `THIRD-PARTY-LICENSES.txt`.

## Support

If this tool saved you time, a coffee is always appreciated — but it's free forever either way. 🙏
[ko-fi.com/pogeo](https://ko-fi.com/pogeo)

## Verifying your download

Each release's notes include a SHA-256 checksum for the release zip. To check the file you downloaded matches:

```powershell
Get-FileHash "EquipSlotConverter-v1.0.4.zip" -Algorithm SHA256
```

## Disclaimer

The only download the author stands behind is this repository's [Releases page](../../releases/latest). Verify the SHA-256 checksum before unzipping. Beyond that, the tool is provided as-is, with no warranty — use it at your own risk. The author isn't responsible for pre-existing issues on your device (a system that was already compromised, infected, or misconfigured before running this tool), for anything your own antivirus/security software should be handling, or for any damage to your mods, save data, or game installation.

This tool doesn't request admin rights, doesn't touch anything outside your chosen mod folders and its own settings file, and doesn't connect to the network except when you click the Ko-fi link yourself. It never modifies your original mod files — it always writes its output to a new folder. Still, it rebuilds and rewrites binary game files, so mistakes are possible: keep a backup of your Mods folder, and test a converted result in-game before assuming it's correct.
