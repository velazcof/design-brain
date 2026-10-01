
These three principles control how quickly an interface communicates **importance, stability, and structure**.

✔️ Good design uses contrast to direct attention, balance to distribute visual weight, and alignment to create invisible order.

❌ Bad design makes everything compete equally, feel visually lopsided, or look subtly misaligned.


### Contrast

Contrast is the difference between elements. It can come from **value, size, weight, hue, shape, or texture**.

|Contrast Type|What it Communicates|Example|
|---|---|---|
|**Value**|Light vs. dark importance|Dark heading on a light background|
|**Size**|Relative importance|`32px` heading vs `16px` body text|
|**Weight / Style**|Emphasis within the same size|Bold phrase inside regular body text|
Use contrast to make the important thing stand out rather than making secondary content too faint.

For accessibility, WCAG 2.2 AA requires:

- `4.5:1` for normal text
- `3:1` for large text


### Balance

Balance is how **visual weight** is distributed across a layout.

|Type|Feel|Common Use|
|---|---|---|
|**Symmetrical**|Stable, formal, predictable|Dialogs, empty states, dashboards|
|**Asymmetrical**|Dynamic, modern, energetic|Landing pages, marketing, editorial|
|**Radial**|Focused around a center|Circular navigation, progress indicators|
|**Mosaic**|Weight spread evenly across the canvas|Dense dashboards, maps|

Visual weight increases with things like larger size, darker value, higher saturation, complexity, texture, or isolation.


### Alignment

Alignment gives the interface an invisible structure.

|Alignment Type|Use|
|---|---|
|**Edge Alignment**|Mechanically lining up edges to the same axis|
|**Optical Alignment**|Slightly adjusting elements so they _look_ aligned|
|**Left Alignment**|Body text, forms, lists, tables|
|**Center Alignment**|Short isolated content like empty states or hero copy|
|**Right Alignment**|Numeric data, some chat layouts, RTL interfaces|

Use a small number of consistent alignment axes across the page. Different random indents and padding values make a layout feel noisy even when users cannot explain why.


### How They Work Together

A useful order is:

1. **Alignment** — establish structure.
2. **Balance** — distribute visual weight.
3. **Contrast** — direct attention.

Changing one can affect the others. For example, making a CTA much brighter increases its visual weight, which may change the balance of the whole composition.


### Common Mistakes

- **Using low contrast to de-emphasize content.**  
    Reduce size, weight, or position instead of making text hard to read.
    
- **Defaulting to symmetry everywhere.**  
    Symmetry should match the tone of the interface, not just be the easiest layout.
    
- **Decorative misalignment.**  
    Breaking alignment accidentally creates noise, not creativity.
    
- **Overusing centered text.**  
    Center alignment works well for short display copy, but long paragraphs become harder to scan.
    
- **Treating accessibility contrast as a final audit.**  
    Contrast should be considered while defining colors and components, not patched at the end.