
Visual hierarchy is the practice of making an element's **visual importance match its actual importance**. 

✔️ A good hierarchy makes the most important content noticeable first and guides attention in a clear order.

❌ A bad hierarchy gives the wrong elements too much emphasis, makes everything compete equally, or leaves the user unsure where to look next.


### Core Ideas

|Tool|What it communicates|How to use it|Example|
|---|---|---|---|
|**Size**|Importance|Make primary content noticeably larger than supporting content. Relative difference matters more than absolute size.|A `48px` hero heading, `24px` section heading, and `16px` body text.|
|**Weight**|Emphasis|Use heavier font weights to reinforce importance. Establish hierarchy with size first, then weight.|A semibold project title with regular-weight description text underneath.|
|**Color & Contrast**|Attention|High-contrast or saturated elements advance; muted elements recede. Keep secondary content accessible.|White heading text, light-gray body text, and a bright accent color for the primary CTA.|
|**Spacing & Proximity**|Relationships|Keep related elements close together and separate unrelated groups with more whitespace.|A project title sits `8px` above its description, while the next project begins `48px` lower.|
|**Position**|Reading order|Place important information where users naturally encounter it first and create a clear path through the interface.|Your name and role appear at the top of the hero before projects, experience, and contact details.|
|**Shape & Surface**|Prominence|Backgrounds, borders, cards, buttons, and other containers add visual weight. Use them when they communicate meaning, not just decoration.|A filled primary button attracts more attention than a plain text link; a card background groups one project together.|

### Three-Level Hierarchy

|Level|Purpose|Examples|
|---|---|---|
|**Primary**|The main thing the user should notice first.|Hero headline, page title, main CTA, important status|
|**Secondary**|Supporting or structural information that helps organize the page.|Section headings, navigation, supporting copy|
|**Tertiary**|Useful but lower-priority information that should visually recede.|Dates, metadata, captions, labels, secondary details|

Every element does not need to map to exactly three font sizes. The idea is that the **perceived importance** of content should usually fall into a small number of clear tiers.


> [!When reviewing a design]
> 
> - What is the **single most important thing** on this screen?
> - What should the user notice second?
> - Are there obvious primary, secondary, and tertiary levels?
> - Am I using size before reaching for bold or color?
> - Does spacing communicate which elements belong together?
> - Is anything visually louder than its actual importance?
> - If I remove all color, does the hierarchy still work?
> - If I squint at the screen, does the intended structure remain obvious?


### Typography

A strong typographic hierarchy uses:

- Meaningfully different sizes
- Different weights
- Appropriate line heights
- Consistent treatment

Avoid tiny differences such as: ```16px 17px 18px```
Prefer clearly differentiated levels such as: ```14px 18px 28px 40px ```

**The exact numbers are less important than the visible distinction.**


### Accessibility

Visual hierarchy and semantic hierarchy should agree. If something visually behaves like the main heading, it should generally also be represented appropriately in HTML:

```
<h1>...</h1>
<h2>...</h2>
```

not just visually enlarged `<div>` elements.

Hierarchy should also remain understandable without relying exclusively on color, hover states, or extremely low contrast.


### Common Mistakes

- **Everything has the same visual weight.**  
    Nothing stands out, so the user has to determine importance manually.
	
- **Too many things are emphasized.**  
    If everything is important, nothing is important.
    
- **Overusing bold.**  
    Bold loses its meaning when used everywhere.
    
- **Using color to compensate for weak hierarchy.**  
    Fix size, spacing, and structure first.
    
- **Using extremely low contrast for secondary content.**  
    Recessive information still needs to be readable.
    
- **Making hierarchy visible only on hover.**  
    Structure should be understandable before interaction.
    
- **Making the wrong thing visually dominant.**  
    Visual prominence should reflect actual importance.