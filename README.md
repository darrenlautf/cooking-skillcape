# The Cooking Skill: 1–99 at home, 100–120 in the wild

A RuneScape-style cooking curriculum — from zero experience to leading a kitchen
worth a special journey. Single-file static site, no build, no dependencies.

- **Levels 1–99** (skillcape): twelve tiers of home mastery — knife work, stocks,
  sauces, bread, butchery, world cuisines, pastry, the line.
- **Levels 100–120** (master cape): three elite tiers that can only be earned in
  professional kitchens — the brigade, sous chef, the restaurant.
- Real RuneScape XP curve (99 = 13,034,431 xp; 120 = 104,273,167 xp), tuned so
  each tier lands exactly on its band top.
- Rep-based quests (×N on separate days), eight sub-discipline stats, boss
  exams graded on a 0–4 rubric.
- Progress saves in localStorage, per browser.

Merged from three independently generated AI curricula (Claude Fable 5, Codex,
Grok), cross-checked against Le Cordon Bleu Basic→Superior, the CIA Professional
Chef progression, and Michelin's published five criteria.

## Deploy

Any static host works — it's one HTML file.

```sh
# GitHub Pages (after `gh auth login`):
gh repo create cooking-skillcape --public --source . --push
gh api -X POST repos/{owner}/cooking-skillcape/pages -f "source[branch]=main" -f "source[path]=/"
```

Or drag `index.html` onto Netlify Drop / tiiny.host.
