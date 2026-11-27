
Container queries allow components to adapt to their **local environment rather than the entire viewport**. This makes components more reusable across different layouts.

✔️ A good responsive component adapts to the space and context it receives.

❌ A bad responsive component resizes at hardcoded breakpoints with no context of its parent size.

### Types of Queries

| Query | What it checks | Typical Use |
|---|---|---|
| `@media` | Viewport dimensions or user preferences | Navigation, page structure, reduced motion |
| `@container` | Available space within an ancestor | Card layouts, reusable components |
| `@container style()` | An ancestor's computed CSS property value | Component variants, contextual theming |

These techniques complement each other rather than acting as replacements.


### Container Size Queries

A component can change its layout depending on how much room its container provides.

```css
.project-wrapper {
  container: project / inline-size;
}

.project-card {
  display: flex;
  flex-direction: column;
}

@container project (min-width: 500px) {
  .project-card {
    flex-direction: row;
  }
}
```

The same project card can display vertically in a narrow sidebar and horizontally in a wide content area, even on the same screen.

| Container Type | Behaviour |
|---|---|
| `inline-size` | Enables queries along the inline axis (normally width) |
| `size` | Enables queries along both axes, with size containment |
| `normal` | Default; permits style queries but not size queries |

Name containers when nesting them to avoid querying an unintended ancestor.


### Container Query Units

Similar to viewport units, but relative to an eligible query container.

| Unit | Meaning |
|---|---|
| `cqw` | 1% of container width |
| `cqh` | 1% of container height |
| `cqi` | 1% of container inline size |
| `cqb` | 1% of container block size |
| `cqmin` | Smaller of `cqi` and `cqb` |
| `cqmax` | Larger of `cqi` and `cqb` |

These can be combined with `clamp()` for component-relative fluid typography and spacing.

```css
.project-title {
  font-size: clamp(1rem, 0.75rem + 3cqi, 2rem);
}
```


### Style Queries

Style queries allow descendants to change their styling based on a computed CSS property value of an ancestor.

```css
.featured-section {
  --variant: featured;
}

@container style(--variant: featured) {
  .project-title {
    font-weight: 700;
  }

  .project-card {
    border: 2px solid currentColor;
  }
}
```

Unlike ordinary CSS variables, which provide reusable values, style queries allow **conditional styling based on those values**.

This is useful for contextual themes, component variants and avoiding unnecessary prop drilling for visual styling.

Elements are eligible style query containers by default, so explicitly declaring `container-type` is not required for style queries.

Check browser compatibility before using style queries in production.


### Common Mistakes

- **Using viewport queries for every component.**  
  A wide viewport does not guarantee that a component has enough room.

- **Querying the container itself.**  
  Container queries style descendants, not the queried container itself.

- **Leaving nested containers unnamed when targeting a specific ancestor.**  
  A query may resolve against a different ancestor than intended.

- **Using `container-type: size` unnecessarily.**  
  Prefer `inline-size` unless both dimensions need to be queried, since size containment affects content-driven sizing.

- **Ignoring accessibility when using fluid units.**  
  Test typography at 200% zoom and ensure layouts reflow correctly at a `320px` CSS viewport width.