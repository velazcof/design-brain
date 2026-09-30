
Grids create a consistent structure for **alignment, spacing, proportion, and grouping** across an interface.

✔️ A good layout uses the grid to support the content.

❌ A bad layout forces content into arbitrary columns or breakpoints just because the grid says so.


### Grid Anatomy

|Term|Meaning|Example|
|---|---|---|
|**Column**|A vertical subdivision of layout space|One section of a 12-column grid|
|**Gutter**|Space between columns|`24px` between two content columns|
|**Margin**|Space between content and the outer edge|`32px` page padding|
|**Max Width**|Maximum width content can grow to|Centering content inside a `1200px` container|
|**Baseline Grid**|Repeating vertical spacing rhythm|Using `4px` or `8px` increments|


### Spacing Systems

Use a small reusable spacing scale instead of inventing values everywhere.

```
4, 8, 16, 24, 32, 48, 64
```

This creates consistent rhythm and makes components feel related.


### 12-Column Grids and Intrinsic Layout

12-column grids became common because 12 divides cleanly into 2, 3, 4, and 6, making page-level subdivision flexible.

They are still useful for large layout structure, but components should not be forced into arbitrary column counts if that makes their content awkward.

Intrinsic layouts are based on the **natural size needs of the content**, rather than fixed device layouts.

```
grid-template-columns:
  repeat(auto-fit, minmax(280px, 1fr));
```

This means each column should stay at least `280px` wide, while the browser fits as many columns as available space allows.


### Layout and Hierarchy

Layout itself can communicate importance.

- **More width** usually gives an element more visual weight.
- **Closer spacing** suggests elements belong together.
- **More whitespace** creates separation and emphasis.
- **Shared alignment** makes the page feel structured.
- **Breaking the grid** can create emphasis when done deliberately.

Some common layout patterns are:

|Pattern|Typical Use|
|---|---|
|**Pancake Stack**|Vertically stacked sections|
|**Sidebar Layout**|Docs, dashboards|
|**RAM Grid**|Responsive card layouts using `auto-fit/minmax()`|
|**Masonry**|Variable-height galleries or feeds|


### Responsiveness

|Tool|Responds To|Typical Use|
|---|---|---|
|**Media Query**|Viewport size|Overall page structure|
|**Container Query**|Component container size|Reusable components|
|**Intrinsic Layout**|Available space and content constraints|Flexible card grids|
Breakpoints should happen where the **content stops working well**, not just because a width matches a common phone, tablet, or desktop size.


### Density

| Density         | Typical Use                             |
| --------------- | --------------------------------------- |
| **Comfortable** | Portfolios, marketing sites, onboarding |
| **Cozy**        | Productivity apps                       |
| **Compact**     | Dashboards, tables, admin tools         |
Density should match the product. A portfolio usually benefits from more breathing room than a data-heavy dashboard.


### Common Mistakes

- **Forcing everything into a 12-column grid.**  
    Use the grid for structure, but let components follow their own content needs.
    
- **Using arbitrary spacing values.**  
    A spacing scale creates stronger rhythm and consistency.
    
- **Choosing breakpoints by device category only.**  
    Break the layout where the content actually starts to fail.
    
- **Stretching content too far on large screens.**  
    Use max-width constraints so text and sections stay readable.
    
- **Making components depend only on viewport width.**  
    A reusable component should adapt to the space it actually receives.
    
- **Breaking alignment accidentally.**  
    Grid-breaking creates emphasis only when the surrounding structure is otherwise consistent.