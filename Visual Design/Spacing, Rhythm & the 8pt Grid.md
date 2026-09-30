
Spacing creates **grouping, rhythm, and hierarchy** before the user consciously reads the interface.

✔️ A good spacing system uses a small, repeatable scale.

❌ A bad one relies on arbitrary values like `13px`, `19px`, or `27px` chosen by eye.


### The 8pt Grid

A common spacing system uses multiples of `8px`, with `4px` as a smaller half-step for tighter UI.

|Token|Value|Typical Use|
|---|---|---|
|`space-1`|4px|Icon gaps, badges, tight inline spacing|
|`space-2`|8px|Small internal padding|
|`space-3`|12px|Medium component padding|
|`space-4`|16px|Default padding, list spacing|
|`space-5`|24px|Card padding, related groups|
|`space-6`|32px|Between content groups|
|`space-7`|48px|Between major sections|
|`space-8`|64px|Large page-level spacing|
|`space-9`|96px|Hero and major section spacing|

The exact scale can vary. The important part is having **limited, intentional choices** instead of arbitrary spacing everywhere.


### Spacing and Meaning

Spacing is semantic because distance communicates relationships.

|Relationship|Typical Spacing|
|---|---|
|Elements inside one component|4–8px|
|Related components|16–24px|
|Separate content groups|32–64px|
|Major page sections|64–96px|

This is Gestalt proximity in practice: tighter spacing says **“these belong together”**, while larger spacing says **“this is a separate group.”**

For responsiveness, component spacing should usually remain predictable, while page-level spacing can become more generous as more space becomes available.

| Approach     | How it Works                                | Best Use                           |
| ------------ | ------------------------------------------- | ---------------------------------- |
| **Fixed**    | Same token value everywhere                 | Buttons, inputs, component padding |
| **Adaptive** | Switch spacing values at breakpoints        | Larger layout changes              |
| **Fluid**    | Spacing grows smoothly with available space | Heroes and major page sections     |


### Padding, Gap & Margin

A useful rule is:

> **Components own their internal padding; layouts own the spacing between components.**

For example, a card defines its own padding, while the parent layout uses `gap` to control the distance between cards.

```
.card {
  padding: 24px;
}

.card-list {
  display: flex;
  gap: 32px;
}
```

Using `gap` for sibling spacing generally keeps reusable components cleaner than giving individual components external margins.


### Visual Rhythm

Spacing and typography should feel like they belong to the same system.

For example, `16px` body text with a `24px` line-height works naturally with a spacing scale containing values like:

```
8, 16, 24, 32, 48
```

Repeated relationships like these create a calmer, more consistent vertical rhythm.


### Common Mistakes

- **Using random one-off values.**  
    Repeated nudging creates an inconsistent spacing system.
    
- **Using margin for all sibling spacing.**  
    Prefer parent-controlled `gap` where possible.
    
- **Inconsistent component padding.**  
    Similar components should draw from the same spacing scale.
    
- **Over-spacing small screens.**  
    Large desktop gaps can consume too much of a mobile viewport.
    
- **Using only fixed** `**px**` **values around scalable text.**  
    Text-containing elements may benefit from relative units such as `rem` so their spacing can grow with text size.