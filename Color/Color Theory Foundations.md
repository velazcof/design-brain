
Color helps communicate **attention, hierarchy, meaning, and mood**. A good palette is not just a set of nice-looking colors — the colors need to work together and remain readable in context.

✔️ Good color systems use consistent relationships between hue, lightness, and chroma.

❌ Bad color systems rely on random swatches, excessive saturation, or color alone to communicate meaning.


### Color Models

|Model|Best Use|
|---|---|
|**sRGB / Hex**|Standard screen output and compatibility|
|**HSL**|Simple manual color picking|
|**OKLCH**|Building perceptually consistent modern palettes|
|**Display P3**|Wider-gamut colors on compatible displays|

OKLCH is especially useful for tonal scales because its lightness values behave more consistently with human perception.


### Color Harmony

|Harmony|Relationship|Feel|
|---|---|---|
|**Complementary**|Opposite hues|Strong contrast, energetic|
|**Analogous**|Nearby hues|Calm, cohesive|
|**Triadic**|Three evenly spaced hues|Vibrant, balanced|
|**Split-complementary**|Base hue + colors beside its opposite|Contrast with less tension|

Harmony gives you **candidate hues**, not a finished palette. You still need to decide lightness, chroma, proportion, and context.


### Tonal Scales

A tonal scale creates lighter and darker versions of a color.

```
50 → very light
100
200
...
800
900 → very dark
```

In OKLCH, vary **lightness** while keeping the hue relatively stable, and usually reduce chroma near the lightest and darkest ends.


### Chroma & Visual Weight

- **High chroma** → accents, states, important interactive elements
    
- **Medium chroma** → brand and primary colors
    
- **Low chroma** → backgrounds, surfaces, neutral areas

Highly vivid colors attract attention, so their impact decreases when they are used everywhere.


### Color & Meaning

Common UI conventions include:

- Red → error / danger
    
- Green → success
    
- Amber → warning
    
- Blue → information / interaction
    
- Gray → secondary or disabled content

These meanings depend on culture and context, so **color should never be the only signal**. Pair it with text, icons, shape, or another visual cue.


### Accessibility

WCAG 2.2 AA contrast targets:

- **4.5:1** for normal text
- **3:1** for large text and many UI elements

Accessibility should be considered while creating the palette, not added afterward.