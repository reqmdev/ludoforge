# LudoForge UI

LudoForge UI is a Codex / GPT-5.5 skill for designing game interfaces without generic AI UI patterns.

It is made for game menus, lobbies, HUDs, inventories, shops, character customization screens, matchmaking screens, settings screens, onboarding screens, and result screens.

The goal is simple: make the AI choose a real game theme, stay loyal to that theme, and design the interface around the player's next action instead of producing random neon, glass panels, dashboard cards, fake premium gradients, or generic game UI decoration.

## What this skill improves

- Keeps the UI tied to one clear game theme.
- Prevents SaaS/dashboard layouts from leaking into game screens.
- Forces better hierarchy for Play, Ready, Invite, Equip, Claim, Continue, and other core actions.
- Makes the AI think about player intent, screen purpose, and state clarity.
- Reduces common AI slop such as meaningless badges, random glow, overdesigned cards, fake urgency, and theme drift.
- Works for many game styles instead of only one fixed theme.

## What it is not

This is not a visual asset pack, component library, or game engine plugin. It is a skill file that gives Codex stronger design rules when it writes or edits game UI code.

## Installation

Install the skill with the skills CLI.

### Global install for all supported agents

Use this if you want the skill to be available globally, not only for Codex:

```powershell
npx skills add reqmdev/ludoforge -g --all -y
```

### Codex-only global install

Use this if you only want to install it globally for Codex:

```powershell
npx skills add reqmdev/ludoforge -g -a codex -y
```

### Current project only

Use this inside a project folder if you only want the skill available for that project:

```powershell
npx skills add reqmdev/ludoforge -a codex -y
```

Meaning of the flags:

- `-g` installs it globally.
- `--all` installs it for all supported agents/tools.
- `-a codex` installs it only for Codex.
- `-y` accepts prompts automatically.

After installing, restart Codex or your AI tool if the skill does not appear immediately.

## Check installation

Run:

```powershell
npx skills list
```

You should see `ludoforge-ui` in the list.

## How to use in Codex

You can call it directly in a Codex prompt:

```text
Use the ludoforge-ui skill. Design a browser multiplayer game lobby screen.
```

A better project prompt:

```text
Use the ludoforge-ui skill. Redesign the current game lobby screen. Read the existing components, CSS variables, Tailwind config, assets, and current layout first. Keep the existing project structure. The player should understand the primary action within 3 seconds, and the UI must stay faithful to one clear game theme.
```

## Example use cases

- Redesign a multiplayer lobby.
- Build a main menu for a browser game.
- Improve a HUD without blocking gameplay.
- Create an inventory or loadout screen.
- Design a cosmetic shop or battle pass screen.
- Make a character customization screen.
- Improve a match result or reward screen.

## Core principle

Game UI is not SaaS UI with a skin. It must support a play loop, a mood, a world, and fast player decisions.

Do not make the UI louder to make it feel like a game. Make it more specific: specific theme, specific player action, specific hierarchy, and specific state language.
