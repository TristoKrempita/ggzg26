# ggzg26 — CS2 LAN config

1. Log into Steam on the LAN PC, launch CS2 once, quit.
2. For each file below: open it on GitHub → click **Raw** → Ctrl+A, Ctrl+C → paste into Notepad → **Save As** to the folder listed. In Save As: **Save as type** = `All Files`, **Encoding** = `UTF-8`, **filename in double quotes** (e.g. `"autoexec.cfg"`) so Notepad doesn't add `.txt`.

| File | Paste into |
| --- | --- |
| `cs2_user_keys_0_slot0.vcfg` | `C:\Program Files (x86)\Steam\userdata\111934044\730\local\cfg\` |
| `cs2_user_convars_0_slot0.vcfg` | `C:\Program Files (x86)\Steam\userdata\111934044\730\local\cfg\` |
| `cs2_video.txt` | `C:\Program Files (x86)\Steam\userdata\111934044\730\local\cfg\` |
| `autoexec.cfg` | `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\` |

3. Steam → right-click CS2 → Properties → Launch Options, add: `+exec autoexec`
4. Launch. If anything looks off, open console and run `exec autoexec`.

If Steam is on a different drive on the LAN PC, swap `C:\Program Files (x86)\Steam` for wherever it lives.

## Heads-up on folders

Three different top-level folders are involved — don't mix them up:

| Folder | What it's for |
| --- | --- |
| `userdata\111934044\730\local\cfg\` | The 3 `cs2_*` files go here. This is what the game reads at launch. |
| `userdata\111934044\730\remote\` | **Don't touch.** Steam Cloud's sync area — Steam manages it. |
| `steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\` | CS2 game install. `autoexec.cfg` goes here, triggered by `+exec autoexec`. |
