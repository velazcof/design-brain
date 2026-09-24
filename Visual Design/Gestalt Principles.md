
People perceive visual relationships and groups before they consciously read an interface. 
Gestalt principles help make the structure of a UI obvious.

### The 6 UI Principles

| Principle     | Core question answered          | Primary UI application                              |
| ------------- | ------------------------------- | --------------------------------------------------- |
| Proximity     | What belongs together?          | Form layout, button groupings, section spacing      |
| Similarity    | What is the same type of thing? | Interactive state styling, typographic roles        |
| Closure       | What shape is implied?          | Icon design, progress indicators, peek patterns     |
| Figure/Ground | What is the focus vs. context?  | Modals, cards, contrast requirements                |
| Common Region | What is enclosed together?      | Card components, panels, toolbars                   |
| Continuity    | What is the reading path?       | Reading order, steppers, column alignment, patterns |


> [!NOTE] When reviewing a design
> - Can I identify the groups without reading?
> - Are related things closer together?
> - Do things that look the same behave the same?
> - Am I adding borders/cards where spacing alone would work?
> - Does the eye naturally know where to go next?

### Gestalt and Hierarchy

Proximity and Similarity answer “what belongs together?” while size, weight, and contrast answer “what is most important?”

**Gestalt grouping must agree with intended meaning before hierarchy styling is applied.** Fix the spatial relationships first, then layer typographic and color hierarchy on top.


### Common Mistakes

- **Using only one Gestalt cue.** Don’t rely only on color, spacing, borders, etc. Good grouping usually has at least two reinforcing cues, like proximity + similarity, or common region + proximity. That makes the grouping more robust and accessible.

- **Forgetting that dark mode changes figure/ground.** You can’t just invert colors. Raised surfaces like cards and modals still need to visually separate from the background, usually through luminance/elevation differences rather than shadows alone.

- **Forcing content into a rigid grid.** The layout system shouldn’t break natural groupings. If three controls belong together, don’t spread them apart just because a 12-column grid says so. Content relationships should drive layout.

- **Creating too many visual groups.** If everything is boxed, highlighted, carded, sectioned, bordered, or separated, nothing feels important anymore. The page suggests roughly **3–5 meaningful regions per screen** as a useful target.

- **Adding separators when spacing would already work.** If two sections are sufficiently far apart, you may not need a border or divider at all. Extra separators can just create noise.
