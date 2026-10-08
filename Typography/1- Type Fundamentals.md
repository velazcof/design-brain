
Typography is not just choosing a nice font. Good UI typography depends on **legibility, sizing, spacing, hierarchy, and choosing the right typeface for the job**.

✔️ Good typography makes content easy to read, establishes clear hierarchy, and gives the interface a consistent visual voice.

❌ Bad typography uses fonts, sizes, weights, or spacing that look inconsistent, reduce readability, or make the content hierarchy unclear.


### Typeface Categories

|Category|Characteristics|Typical Use|
|---|---|---|
|**Serif**|Small finishing strokes on letters|Editorial, long-form reading, expressive headings|
|**Sans-serif**|Clean strokes without serifs|UI, apps, dashboards, portfolios|
|**Monospace**|Every character takes equal horizontal space|Code, terminals, tabular data|
|**Display / Decorative**|Highly expressive letterforms|Large headings and branding|

For interfaces, humanist sans-serifs such as Inter tend to work well because their letterforms remain distinct at small sizes.


### Typeface vs. Font

|Term|Meaning|
|---|---|
|**Typeface**|The overall design family, e.g. Inter or Garamond|
|**Font**|A particular instance or style within that family|
|**Font Family**|The collection of related styles and weights|
|**Font File**|The actual `.woff2`, `.ttf`, or `.otf` file loaded by software|
In casual use, _font_ and _typeface_ are often used interchangeably.


### Font Size & Line Height

Font size controls the general scale of the text, while **line-height** controls the vertical distance between lines.

```
body {
  font-size: 1rem;
  line-height: 1.5;
}
```

Typical starting points:

|Content|Line Height|
|---|---|
|**Body text**|`1.4–1.6`|
|**Large headings**|`1.1–1.25`|

Unitless line-height is usually preferred because it scales automatically with the font size.


### px, em & rem

|Unit|Relative To|Typical Use|
|---|---|---|
|**px**|Fixed CSS pixel|Borders, icons, small fixed dimensions|
|**em**|Current/parent font size|Spacing that should scale with local text|
|**rem**|Root font size|Font sizes and global typography|

Prefer `rem` for text sizing so typography can respect user font-size preferences and zoom settings.


### Kerning & Tracking

**Kerning** adjusts spacing between specific letter pairs:

```
AV   To   WA
```

**Tracking** (`letter-spacing`) adjusts spacing across an entire piece of text.

Tracking is useful for things like all-caps labels, but adding lots of spacing to normal body text can hurt readability.


### Typographic Hierarchy

Hierarchy should usually combine multiple properties rather than relying on size alone.

|Variable|Example|
|---|---|
|**Size**|Heading larger than body text|
|**Weight**|Heading semibold, body regular|
|**Color**|Secondary text slightly muted|
|**Spacing**|More space before major headings|

For example:

```
Large + Bold       → Primary
Medium + Semibold  → Secondary
Small + Regular    → Supporting
```

Using at least two cues makes the hierarchy clearer without requiring enormous size differences.


### Type Scales

A type scale is a limited set of font sizes used consistently throughout a design.

```
14px → Small
16px → Body
20px → H3
25px → H2
31px → H1
```

The exact numbers matter less than having **clear, repeatable levels** instead of choosing a new size for every element.


### OpenType Features

Fonts can contain additional typographic behaviour and alternate glyphs.

|Feature|Use|
|---|---|
|**Ligatures**|Combine pairs such as `fi` for cleaner shapes|
|**Tabular Figures**|Give numbers equal width for tables and dashboards|
|**Oldstyle Figures**|Numbers designed to blend into body text|
|**Small Caps**|Properly designed smaller capital letters|

These features are usually subtle, but they can improve polish in specific contexts.


### Variable Fonts

A variable font can contain a range of weights, widths, or other properties inside one font file instead of requiring separate files for every style.

```
Weight:
100 ───────────── 900
```

This allows typography to vary fluidly and can simplify font loading.


### Contrast & Accessibility

For WCAG 2.2 AA:

- Normal text requires at least **4.5:1** contrast.
- Large text requires at least **3:1**.

Do not make supporting text unreadably faint just to reduce its visual importance. Use size, weight, and spacing as well.


### Common Mistakes

- **Using decorative fonts for body text.**  
    Expressive fonts usually work better at display sizes.
    
- **Relying only on font size for hierarchy.**  
    Combine size with weight, color, or spacing.
    
- **Using overly tight line-height for paragraphs.**  
    Body text needs enough vertical breathing room.
    
- **Adding excessive letter-spacing to body text.**  
    It disrupts word shapes and slows reading.
    
- **Using tiny or low-contrast supporting text.**  
    De-emphasis should not come at the cost of readability.
    
- **Choosing fonts only because they look nice.**  
    Consider how well the letterforms perform at the sizes and context where they will actually be used.