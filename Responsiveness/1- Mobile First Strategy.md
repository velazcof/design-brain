
Mobile-first means designing and styling for the **smallest useful layout first**, then progressively adding space, structure, and features as more room becomes available.

✔️ A good mobile-first design prioritises the essentials first and enhances naturally as space grows.

❌ A bad one designs desktop first, then hides or squeezes content until it technically fits on mobile.

### Modern Responsive Approach

|Concern|Modern Approach|
|---|---|
|**Base styles**|Start with the smallest layout|
|**Breakpoints**|Add them where content starts to struggle|
|**Page layout**|Use viewport media queries when needed|
|**Components**|Prefer container queries for local responsiveness|
|**Flexible grids**|Use intrinsic CSS like `minmax()`, `auto-fit`, and `flex-wrap`|
|**Typography**|Use fluid sizing such as `clamp()`|
|**Touch targets**|Keep interactive elements comfortably tappable|

Modern responsive design uses fewer arbitrary device categories and lets content adapt more naturally to available space.


### Mobile-First CSS

Write the simplest layout as the default, then enhance upward:

```
.card {
  display: block;
}

@media (min-width: 48rem) {
  .card {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
```

This is generally easier to reason about than building a complex desktop layout and repeatedly undoing it for smaller screens.


### Content-Driven Breakpoints

Do not automatically think:

```
375px  → phone
768px  → tablet
1024px → laptop
```

Instead, resize the layout and add a breakpoint when something actually stops working well:

- navigation becomes cramped
- cards become too narrow
- text becomes uncomfortable to read
- columns need to stack

Prefer `rem`/`em` breakpoints when practical so they respond better to font scaling and zoom.


### Responsive Tools

|Tool|Best For|
|---|---|
|**Intrinsic CSS**|Layouts that can reorganise themselves|
|**Container Queries**|Components reacting to their own available width|
|**Media Queries**|Larger page-level structural changes|
|`**clamp()**`|Fluid typography and spacing|

These tools complement each other rather than replacing one another.


### Mobile-First ≠ Mobile-Only

Starting small does not mean desktop is an afterthought.

Larger screens should gain useful enhancements such as:

- more visible navigation
- multi-column layouts
- additional context
- more efficient use of space

The goal is to **start constrained, then enhance upward**, while still designing every size intentionally.


### Common Mistakes

- **Using device-specific breakpoints by default.**  
    Let the content determine when the layout should change.
    
- **Making every responsive change with media queries.**  
    Intrinsic CSS and container queries can handle many cases more cleanly.
    
- **Treating mobile as a compressed desktop.**  
    Prioritise content rather than simply hiding things.
    
- **Ignoring desktop because the process started mobile-first.**  
    Large screens still need deliberate composition.
    
- **Making touch targets too small.**  
    Touch interfaces need significantly more clickable area than mouse-driven ones.