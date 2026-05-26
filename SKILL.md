---
name: ludoforge-ui
description: Prevents generic AI/Codex game UI patterns when generating game frontend code. Use this skill whenever building or redesigning game menus, lobbies, HUDs, inventories, shops, character screens, matchmaking screens, settings, onboarding, result screens, or browser/desktop/mobile game interfaces. It forces theme fidelity, readable game UX, and deliberate art direction instead of generic AI-made neon/glass/dashboard UI.
---

# LudoForge UI

This skill pushes Codex toward deliberate, theme-faithful game interface design.

Generic AI game UI is easy to recognize: oversized glowing panels, cyberpunk gradients, floating glass cards, random fantasy ornaments, fake premium shine, pill buttons everywhere, meaningless badges, cluttered HUDs, hero sections inside menus, dramatic blur backgrounds, and a theme that changes from component to component.

Game UI is not SaaS UI with a skin. It must support a play loop, a mood, a world, and fast player decisions. Build interfaces that feel like they belong to a real game, not a UI template generator.

The goal is not to make everything darker, louder, shinier, or more decorative. The goal is to make every screen more specific: specific theme, specific player action, specific hierarchy, specific state language.

---

## Core Rule

If a UI decision feels like a default AI move, ban it.

Do not replace it with another decorative trick. Replace it with a clearer game-specific decision.

A good game interface should answer these questions before it looks stylish:

- What screen is this?
- What is the player trying to do in the next 3 seconds?
- What information must be visible instantly?
- What theme/world does this belong to?
- Which parts are interactive, locked, selected, urgent, owned, ready, or cosmetic?

If the design cannot answer those questions, it is probably slop.

---

## Mandatory First Pass: Theme Lock

Before writing UI code, establish a compact theme lock. Derive it from the user's brief, existing files, screenshots, assets, design tokens, CSS variables, images, game name, current UI, or genre.

If the user gives no theme, choose one that fits the game genre and screen purpose. Do not ask unless the missing detail blocks implementation.

The theme lock must define:

- **World:** the setting or fiction of the interface.
- **Player fantasy:** what the UI should make the player feel like they are doing.
- **Material language:** wood, parchment, stone, steel, paper, enamel, cloth, plastic, hologram, terminal, carved panels, painted cards, etc.
- **Shape language:** angular, carved, compact, mechanical, ornamental, soft, chunky, tactical, arcade-like, toy-like, gothic, etc.
- **Color family:** 3-6 stable colors, preferably from existing project tokens.
- **Typography direction:** readable game-like text hierarchy, not generic startup typography.
- **Interaction tone:** snappy, cozy, heavy, tactical, mysterious, playful, premium, arcade, horror, etc.
- **Forbidden drift:** 3-5 things that would break the chosen theme.

Once the theme is locked, every panel, button, icon, badge, card, modal, hover state, empty state, loading state, and disabled state must obey it.

Do not mix themes unless the product already does. A gothic lobby cannot suddenly use sci-fi neon panels. A cozy farming UI cannot suddenly use esports HUD shards. A tactical military UI cannot use random cute rounded candy buttons.

---

## Source Priority

When working inside an existing project, read before designing.

Use this priority order:

1. Existing project UI, CSS variables, Tailwind config, component library, screenshots, art assets, sprites, icons, fonts, routes, and naming.
2. User-provided theme or game description.
3. Genre conventions appropriate to the requested screen.
4. A new theme lock you create deliberately.

Do not invent a new visual identity if the project already has one. Do not overwrite the game's tone because an AI pattern is easier to generate.

---

## Game UI Is Not Dashboard UI

Never treat game screens like SaaS dashboards.

A game lobby is not a dashboard. A character screen is not a profile settings page. An inventory is not a data table. A shop is not a pricing page. A match result screen is not an analytics report. A HUD is not a metric-card grid.

Game UI can be clean, but it should still feel game-native. Use restrained theme-specific surfaces, game hierarchy, and interaction states instead of business UI patterns.

---

## Keep It Playable

Readable beats decorative.

- Primary action must be obvious within one glance.
- Secondary actions must be available but quieter.
- Critical status must be visually distinct without screaming.
- Navigation must be predictable.
- The player should not need to read decorative text to understand what to do.
- Do not cover the character, map, lobby, or gameplay focal area with unnecessary panels.
- Important labels must stay legible over art backgrounds.
- If the screen is used often, reduce friction and noise.
- If the screen appears briefly, prioritize immediate comprehension.

A good game screen feels designed for repeated use.

---

## Screen Standards

### Main Menu

A main menu should communicate game identity immediately without becoming a fake cinematic poster.

- Use one clear primary action.
- Keep secondary actions grouped logically.
- Let the background or art carry atmosphere.
- Avoid filling the screen with generic cards.
- Avoid long marketing copy.
- Avoid hero-section structure unless it is actually a landing page.

### Lobby / Matchmaking

A lobby is about readiness, party state, mode selection, social presence, and starting the game.

- Preserve a central stage or focal area for the character, party, map, or selected mode.
- Make readiness, party slots, invite actions, and selected queue unmistakable.
- Keep chat/social panels compact and readable.
- Do not use SaaS sidebars unless the game genuinely has a persistent shell.
- Do not create fake analytics, fake activity feeds, or dashboard stats.

### HUD

A HUD must be fast and minimal.

- Show only information needed during play.
- Respect screen edges and gameplay visibility.
- Use consistent anchors: health/resource bottom or corner, objective top/side, minimap where expected.
- Do not add decorative panels that block gameplay.
- Do not add animated clutter for style.
- Use color and shape consistently for danger, cooldown, selection, ally/enemy, locked/unlocked.

### Inventory / Loadout

Inventory UI is about scanning, comparing, equipping, sorting, and understanding rarity/state.

- Use strong item grid rhythm.
- Show equipped, selected, locked, owned, and new states clearly.
- Keep item details close to the selected item.
- Do not turn inventory into a generic table unless the game is intentionally spreadsheet-like.
- Do not use rarity colors randomly; define them and reuse them.

### Shop / Battle Pass / Rewards

Monetization screens must still feel like the game, not a mobile ad template.

- Make price, ownership, preview, quantity, and purchase action clear.
- Do not overload with glowing best-value stickers unless functional and true.
- Do not use casino-like effects unless the game explicitly uses that tone.
- Keep cosmetic previews large enough to judge.
- Keep reward tracks readable and compact.

### Character / Customization

Character screens need a strong preview area.

- Give the avatar/character breathing room.
- Group cosmetic categories clearly.
- Avoid placing dozens of panels around the character.
- Show locked, unlocked, owned, new, and equipped states clearly.
- Cosmetic items must not imply gameplay power unless the game has that system.

### Results / End Screen

Results screens must quickly answer what happened and what changed.

- Outcome first: win/loss/rank/progression/rewards.
- Then personal contribution, unlocks, next action.
- Avoid fake hype copy.
- Avoid too many celebratory effects around ordinary results.
- Use motion sparingly and only for earned moments.

### Settings

Settings can be plainer than the rest of the game, but still themed.

- Prioritize clarity and accessibility.
- Use conventional controls.
- Do not over-theme controls so much that they become hard to use.
- Separate gameplay, video, audio, controls, account, and accessibility cleanly.

---

## Hard No

Do not use these as default moves:

- No generic neon cyberpunk unless the game is actually neon cyberpunk.
- No glassmorphism shells as the main visual language.
- No floating SaaS dashboard cards.
- No metric-card grids as a first instinct.
- No random premium gradients.
- No blue-purple-black default AI dark mode unless it fits the theme.
- No glowing cyan accent spam.
- No fake charts, fake analytics, or fake operational feeds.
- No hero blocks inside lobbies, HUDs, shops, inventories, or settings.
- No decorative eyebrow labels like LIVE OPS, COMMAND CENTER, PLAYER HUB, or TACTICAL OVERVIEW unless the game voice truly supports them.
- No meaningless status dots.
- No pills everywhere.
- No huge rounded rectangles everywhere.
- No overpadded panels that waste playable space.
- No one-big-card-with-everything layout unless it matches the screen purpose.
- No long marketing copy in functional game screens.
- No random lore snippets that do not help the interface.
- No fake urgency badges.
- No badge spam.
- No reward/confetti effects for normal navigation.
- No blurry radial glow backgrounds used to hide weak composition.
- No copy-pasted mobile game shop patterns unless the target game is that kind of product.
- No generic fantasy parchment slapped onto unrelated UI.
- No generic sci-fi hologram slapped onto unrelated UI.
- No switching material styles between screens without a reason.
- No decorative icons inside circles just to fill space.
- No unnecessary side rails.
- No AI-made esports look: sharp shards, random neon, giant metallic borders, fake sponsor-panel composition.
- No AI cozy look: beige cards, soft blobs, random leaf icons, rounded pill overload.
- No AI gothic look: black-purple gradients, random red glow, bat icons everywhere, illegible ornate text.

---

## Common Codex Game UI Failures

Avoid these failures aggressively:

- Building a lobby as a SaaS dashboard with stats cards and recent activity.
- Making every screen a centered glass panel over a blurred background.
- Using random colored rarity borders without defining rarity behavior.
- Using Play Now as a giant gradient pill regardless of theme.
- Creating fake currencies, fake timers, fake quests, or fake shop labels not requested by the user.
- Treating the game logo area like a startup brand lockup.
- Filling empty areas with lore paragraphs instead of improving layout.
- Placing chat, party, mode select, quests, store, news, and player profile all at equal visual priority.
- Making disabled/locked states look like active premium buttons.
- Using tiny low-contrast text over illustrated backgrounds.
- Creating mobile layouts by stacking every desktop panel vertically.
- Adding hover transforms, bounces, glow pulses, or animated scale effects to every button.
- Designing with CSS effects instead of composition, spacing, and state clarity.
- Using the same radius, border, shadow, and fill on every component.

---

## Normal Game UI Replacements

### Panels

Panels should feel like they are made from the theme's material.

- Gothic: dark carved frames, muted stone/wood surfaces, restrained crimson/amber accents.
- Cozy: warm paper/wood panels, soft but not childish corners, clear separators.
- Sci-fi: purposeful technical surfaces, restrained scan lines or bevels, not random hologram blur.
- Tactical: compact dark panels, readable grids, labels with utility, not fake military cosplay.
- Arcade: bold blocks, simple shapes, strong contrast, controlled saturation.

Use borders, separators, inset surfaces, and texture hints. Do not depend on huge shadows and glows.

### Buttons

Buttons must clearly show action priority.

- Primary button: strongest color/material in the theme.
- Secondary button: quieter surface or outline.
- Destructive/danger button: reserved and consistent.
- Locked button: visibly unavailable, not just lower opacity.
- Ready/play button: always unmistakable.

Avoid pill buttons unless the whole game uses round toy-like shapes.

### Cards

Cards are for selectable content, not decoration. A card should usually represent a mode, item, quest, party member, reward, loadout, map, or cosmetic. If a card has no player decision attached, reconsider it.

### Badges

Badges must mean something.

Good badge meanings: New, Equipped, Locked, Owned, Ready, Invite sent, Rare, Epic, Full, In queue, Limited time, Completed.

Bad badge meanings: Live pulse, Focus, Premium, Control, Active, Online, Snapshot, Night shift, Command, unless they are real game terms.

### Icons

Icons must match the theme and be readable at game UI scale.

- Use consistent stroke/fill style.
- Avoid mixing emoji, outline icons, filled icons, and tiny decorative symbols.
- Do not put every icon inside a rounded square.
- Do not rely on icon-only controls for important actions.

### Typography

Typography must support game tone and readability.

- Use project fonts if present.
- Use a display style only for titles, mode names, or major outcomes.
- Use readable UI text for controls, labels, prices, timers, and descriptions.
- Do not use generic startup headline hierarchy.
- Do not use ornate fonts for dense UI text.

### Color

Color must be systemic. Define colors for background/world layer, main surface, raised or selected surface, primary action, secondary action, danger/warning/success, locked/disabled, text primary/muted, and rarity tiers if used.

Do not invent random colors per component.

### Motion

Motion must communicate state. Use motion for queue started, ready toggled, reward earned, item equipped, modal opened/closed, damage/alert/cooldown feedback. Avoid constant pulsing labels, decorative breathing glows, floating cards, or hover animation on every component.

---

## Theme Palette Starting Points

Use existing project colors first. If there are none, choose or derive from one of these. Do not blindly apply a palette if it conflicts with the game.

| Theme Direction | Background | Surface | Primary | Secondary | Accent | Text |
|---|---|---|---|---|---|---|
| Cozy Gothic Village | `#151016` | `#241a22` | `#b84a62` | `#d39a55` | `#6f8f72` | `#f3e8dc` |
| Vampire Manor | `#100d12` | `#211720` | `#8f2638` | `#b08a5a` | `#6d5a7d` | `#efe4dc` |
| Forest Folk | `#162014` | `#26351f` | `#8faa5f` | `#c9a45d` | `#b76e4a` | `#f0ead8` |
| Arcane Library | `#161323` | `#25213a` | `#8f6fd1` | `#c9a96b` | `#5fa3a0` | `#ece6f5` |
| Tactical Iron | `#121417` | `#20242a` | `#d0a85c` | `#78828e` | `#9a4f45` | `#e8e1d5` |
| Space Utility | `#0c1017` | `#171d27` | `#70a7c7` | `#d0b16d` | `#d36f55` | `#e7edf2` |
| Pirate Map | `#21170f` | `#3a2919` | `#c89b54` | `#7b9c84` | `#b84b3d` | `#f5ead6` |
| Toy Arena | `#24202a` | `#35303d` | `#f0b64c` | `#7fc6a4` | `#e46767` | `#fff4df` |
| Frost Expedition | `#101820` | `#1e2a33` | `#9cc7d9` | `#d6b36a` | `#b95d5d` | `#eef5f7` |
| Desert Relic | `#22180f` | `#372616` | `#c7893b` | `#7f9b68` | `#9d4f3a` | `#f4e6ca` |

Palette discipline matters more than the exact palette.

---

## Component Discipline

Do not generate components just because the screen looks empty.

Every component must be one of these:

- A player action.
- A player choice.
- A status the player needs.
- A preview of something the player owns, selects, or earns.
- Navigation to a real area.
- Feedback from the current game loop.

If a component is only there to look premium, remove it.

---

## Layout Discipline

A game layout should be shaped around the screen's focal object.

Examples:

- Lobby: character, party, map, or mode should dominate; actions wrap around it.
- Inventory: item grid and selected details dominate.
- Shop: product preview and price/action dominate.
- HUD: gameplay view dominates; UI stays peripheral.
- Results: outcome and progression dominate.
- Settings: categories and controls dominate.

Do not start with a sidebar unless the game structure needs it. Do not start with three cards unless the screen is actually choosing between three things. Do not start with a top hero unless the screen is promotional. Do not add a right rail unless the content is persistent and useful.

---

## Copy Rules

Game UI copy should be short and functional.

Allowed examples:

- Play
- Ready
- Invite
- Leave Party
- Find Match
- Equip
- Owned
- Locked
- Claim
- Continue
- Change Mode
- Spectate
- Reconnect
- Match Found

Avoid generic filler:

- Your command center for everything that matters.
- Operational clarity without the clutter.
- A premium experience built for modern players.
- Live pulse.
- Adventure starts here.
- Unlock your potential.

Use game terms only when they belong to the game's actual fiction or mechanics.

---

## Implementation Rules for Codex

When coding:

- Reuse existing components and tokens before creating new ones.
- Preserve project architecture.
- Keep class names semantic and game-specific.
- Keep design tokens centralized.
- Avoid hardcoded random colors spread across components.
- Avoid unnecessary dependencies.
- Avoid fake data unless the user asked for a mockup; mark mock data clearly.
- Make responsive layouts intentionally, not by blindly stacking panels.
- Support keyboard focus and readable contrast.
- Keep hover, focus, active, selected, and disabled states distinct.
- Do not hide important text behind icons or tooltips.
- Do not break gameplay canvas, routing, auth, state, or existing data flows.

---

## Self-Check Before Final Output

Before finishing, audit the UI against this list:

- Does the interface have a locked theme?
- Did every major component inherit that theme?
- Is the primary action obvious?
- Is the player's next step clear?
- Did you avoid SaaS dashboard structure?
- Did you avoid generic glass/neon/gradient slop?
- Did you remove decorative copy?
- Are colors consistent and tokenized?
- Are states clear: selected, active, locked, disabled, ready, owned, new?
- Does the layout protect the game/art/character focal area?
- Would this still make sense after the player sees it 100 times?

If the answer is no, revise before presenting the code.

---

## Final Rule

Do not make the UI louder to make it feel like a game.

Make it more specific.

Specific theme, specific player action, specific hierarchy, specific state language. That is what removes AI slop.
