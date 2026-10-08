
A quick reference for common typography terms used in interface and visual design.

|Term|Meaning|
|---|---|
|**Baseline**|The imaginary line that most letters sit on. It acts as the main reference line for vertical text alignment.|
|**x-height**|The height of the main body of lowercase letters, measured using `x`. A larger x-height usually makes small text feel more legible.|
|**Cap height**|The height of uppercase letters such as `H`, measured from the baseline to the top. Useful when aligning text with icons or other elements.|
|**Ascender**|The part of a lowercase letter that rises above the x-height, as in `b`, `d`, `h`, and `k`.|
|**Descender**|The part of a lowercase letter that drops below the baseline, as in `g`, `p`, `q`, and `y`.|
|**Stem**|A main structural stroke of a letter, usually vertical or diagonal.|
|**Bowl**|A rounded enclosed shape found in letters such as `b`, `d`, `o`, `p`, and `q`.|
|**Counter**|The negative space inside or partly inside a letterform, such as the centre of `o` or the inner space of `e`.|
|**Aperture**|The open gap in partially enclosed letters such as `c` and `e`. Wider apertures can improve clarity at small sizes.|
|**Serif**|A small finishing stroke attached to the end of a letter’s main stroke. Fonts without these are called sans-serif.|
|**Stroke Contrast**|The difference between the thickest and thinnest strokes in a typeface. High contrast can feel elegant, while low contrast often performs better at small UI sizes.|


### Em, rem, and px

|Unit|Relative to|Use case|
|---|---|---|
|`px`|Absolute|Avoid for font sizes. Users who set a larger browser default font size are ignored.|
|`em`|Parent element’s font size|Good for padding and margins that should scale with the local font size.|
|`rem`|Root element’s font size (html)|Preferred for font sizes. Respects the user’s browser font preference.|