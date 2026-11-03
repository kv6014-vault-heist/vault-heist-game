# Blind Spot

Isometric single-player vault heist game. The thief sneaks into a vault, grabs the loot and escapes while avoiding AI guards, CCTV cameras and laser tripwires.

KV6014 Computing Group Project, Group DH5, Northumbria University.

## Team

| Name | Role |
|---|---|
| Arshia Masouleh | Team lead |
| George Hepworth | Developer |
| Owen Wilby | Developer |
| Nathan Oxley | Lead designer |
| Rui (Riley) Caig | Designer |
| Abdulla Al-Nahdi | Cyber consultant, QA |

## Setup

You need **Unreal Engine 5.7** (also available in lab CIS 102) and **Git for Windows**, which includes Git LFS.

First time only:

```
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git lfs install
cd ~/Documents
git clone https://github.com/kv6014-vault-heist/vault-heist-game.git
```

Then open `VaultHeist.uproject`. The first launch is slow while shaders compile.

## Branches

| Branch | Contents |
|---|---|
| `main` | Setup files |
| `owen` | Unreal project, guard AI work |
| `Arshia` | Level blockout |

To get someone's work:

```
git pull
git switch <branch>
git lfs pull
```

## Daily routine

Close Unreal before pulling.

```
git pull
```

Lock a level or Blueprint before editing it, because Unreal files cannot be merged:

```
git lfs lock "path/to/file.umap"
```

When you finish:

```
git add .
git commit -m "what you did"
git push
git lfs unlock "path/to/file.umap"
```

Then add a line to the dev diary.

## Rules

- Work in your own folder and your own test map
- Never edit a file someone else has locked, message them instead
- Small, frequent commits beat one big push at the end of the week
- Commit from your own GitHub account, it is the record of who did what
- Never commit tokens or passwords

## If something breaks

**"Repository not found" when cloning** — you are not signed in. Create a token on GitHub under Settings, Developer settings, Personal access tokens, Tokens (classic), tick `repo`, and use it as your password.

**Push rejected** — someone pushed first. Run `git pull`, then `git push`.

**Textures or levels look broken** — run `git lfs pull`.

**Pasting into Git Bash adds strange characters** — type the command out, or paste with Shift + Insert.

## Assets

All assets must be free and licensed for our use. Add anything new to the approved asset list and tell Abdulla.

| Asset | Creator | Licence |
|---|---|---|
| Wooden Door (door and door frame meshes) | kellett66, via Fab | CC BY 4.0 |


