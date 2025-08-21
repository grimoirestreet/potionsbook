# Staff Instructions: Adding New Potions

## Quick Start
1. Navigate to the `potions-data.json` file in your GitHub repository
2. Click the pencil icon (✏️) to edit
3. Find the appropriate category and add your new potion
4. Commit your changes

## Adding a New Potion

The potions are organized by category. Find the category you want (e.g., "Healing & Medical") and add your new potion to the end of that category's array:

```json
    ,
    {
      "name": "Your Potion Name",
      "difficulty": "Intermediate",
      "restriction": "✅ Students", 
      "effect": "What the potion does - be descriptive",
      "ingredients": "List all ingredients separated by semicolons",
      "instructions": "Step-by-step brewing instructions",
      "time": "How long it takes to brew",
      "notes": "Additional notes, warnings, side effects",
      "appearance": "What the finished potion looks like",
      "duration": "How long effects last",
      "inventor": "Who created it (if known)",
      "source": "What book/reference it's from (if any)"
    }
```

## Field Explanations

### Required Fields:
- **name**: The potion's name (what appears as the title)
- **difficulty**: Must be one of: `"Elementary"`, `"Intermediate"`, `"Advanced"`, `"Master"`
- **restriction**: Who can brew it - examples:
  - `"✅ Students"` - All students allowed
  - `"✅ Year 1"` - Specific year only
  - `"✅ Advanced Students"` - Years 6-7 only
  - `"⚠️ Medical Wing"` - Requires medical supervision
  - `"🚫 Forbidden"` - Completely banned
  - `"🚫 Combat"` - Banned for combat use
- **effect**: What the potion does
- **ingredients**: All ingredients needed
- **instructions**: How to brew it
- **time**: Brewing duration

### Optional Fields (can be left as empty strings `""`):
- **notes**: Additional information, warnings, OOC notes
- **appearance**: Visual description of finished potion
- **duration**: How long effects last
- **inventor**: Who created the potion
- **source**: Reference book or material

## Categories Available

1. **Healing & Medical** - Healing potions, medical treatments
2. **Antidotes** - Antidotes and cures for poisons/conditions
3. **Utility & Academic** - School potions, practical everyday use
4. **Transformation & Disguise** - Appearance-changing potions
5. **Enhancement & Combat (Restricted)** - Combat/enhancement potions
6. **Forbidden & Controlled** - Banned or heavily restricted potions
7. **Player‑Created Potions** - Original creations by players (after approval)

## Example Entry

```json
    ,
    {
      "name": "Concentration Draught",
      "difficulty": "Intermediate",
      "restriction": "✅ Students",
      "effect": "Enhances focus and concentration for studying (2-3 hours)",
      "ingredients": "Ginkgo leaves; powdered crystal; focus herbs; clarity water; ground pearl",
      "instructions": "Steep ginkgo in clarity water → add crystal powder → focus herbs → simmer 30 min → finish with ground pearl",
      "time": "45 minutes",
      "notes": "Popular during exam periods. Do not exceed one dose per day.",
      "appearance": "Clear blue with silver sparkles",
      "duration": "2-3 hours",
      "inventor": "",
      "source": ""
    }
```

## Important Notes

- **Always add a comma** after the previous entry before adding your new one
- **Don't add a comma** after your new entry if it's the last one in that category
- **Check your JSON formatting** - the site will break if there are syntax errors
- **Use straight quotes** (`"`) not curly quotes (`"`)
- **Keep difficulty levels consistent** with the year restrictions

## Difficulty Guidelines

The difficulty system corresponds to Hogwarts year levels and brewing complexity:

- **Elementary**: Years 1-2 students can brew safely
  - Basic potions with simple ingredients
  - Minimal brewing complexity
  - Low danger if mistakes are made
  - Examples: Cure for Boils, Hair-Raising Potion

- **Intermediate**: Years 3-5 students can attempt
  - Moderate complexity requiring more skill
  - Some dangerous ingredients or precise timing
  - Mistakes can cause mild harm or potion failure
  - Examples: Calming Draught, Shrinking Solution

- **Advanced**: Years 6-7 students (Advanced level classes)
  - Complex brewing requiring significant skill
  - Dangerous ingredients or precise techniques
  - Mistakes can cause serious harm
  - Some require special authorization even for advanced students
  - Examples: Polyjuice Potion, Veritaserum

- **Master**: Faculty and trained adults only
  - Extremely complex or dangerous to brew
  - Requires extensive magical knowledge and experience
  - Potentially lethal if brewed incorrectly
  - Often illegal for students to possess
  - Examples: Felix Felicis, Draught of Living Death

### Year Level Correlation:
- **Years 1-2**: Elementary only
- **Years 3-5**: Elementary + Intermediate  
- **Years 6-7**: Elementary + Intermediate + Advanced
- **Post-graduation/Faculty**: All levels including Master

When adding potions, match the difficulty to both the brewing complexity and the appropriate age/skill level for safety.

## Editing Existing Potions

1. Find the potion in the appropriate category in `potions-data.json`
2. Click the pencil icon to edit
3. Modify any of the fields as needed
4. Commit your changes

## Player-Created Potions

For OC potions created by players:
1. Add them to the **"Player‑Created Potions"** category
2. Include detailed approval notes in the `"notes"` field
3. Credit the creating player in the `"inventor"` field

## Troubleshooting

If the site breaks after your changes:
1. Check for missing commas between entries
2. Ensure all quotes are properly closed
3. Verify brackets `{}` are properly matched
4. Look for any special characters that might need escaping
5. Make sure you're adding to the correct category

The site will automatically update within a few minutes of committing your changes to GitHub!
