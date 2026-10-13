
Typographic hierarchy controls **which text gets noticed first, what supports it, and what can safely fade into the background**.

✔️ Good hierarchy makes importance obvious before the user consciously reads everything.

❌ Bad hierarchy makes headings, body text, labels, and metadata compete at similar visual strength.


### Hierarchy Levels

|Level|Purpose|Examples|
|---|---|---|
|**Primary**|The text that should attract attention first|Page title, price, critical status|
|**Secondary**|Supports or structures the primary content|Section headings, card titles, labels|
|**Tertiary**|Detail that can be scanned when needed|Body copy, timestamps, captions|

Usually, a few clear levels work better than many subtle ones.


### Tools for Creating Hierarchy

| Tool                 | Effect                                   | Example                                        |
| -------------------- | ---------------------------------------- | ---------------------------------------------- |
| **Size**             | Strongest signal of importance           | `40px` title vs `16px` body text               |
| **Weight**           | Adds emphasis within similar sizes       | `600` heading vs `400` paragraph               |
| **Contrast**         | Makes text advance or recede             | Bright primary text vs muted metadata          |
| **Spacing**          | Separates topics and groups related text | Large gap before a new section                 |
| **Typeface / Style** | Creates role or personality differences  | Serif display heading + sans-serif body        |
| **Case**             | Can distinguish small labels or metadata | `CURRENT ROLE` above normal sentence-case text |

Use only a few signals at once. If size, weight, color, case, typeface, and spacing all change together, the hierarchy can become noisy.


### Size & Weight

Use **size as the main hierarchy signal**, then reinforce it with weight.

```
48px / 700  → Main heading
28px / 600  → Section heading
16px / 400  → Body text
14px / 400  → Metadata
```

A variable font may allow any weight between values like `300–900`, but the design should still use a **small intentional set** such as `400`, `500`, `600`, and `700`.


### Contrast

High-contrast text feels more important; lower-contrast text recedes.

Do not use extremely faint text just to make something tertiary. Important text should still meet accessibility requirements.

- Normal text: at least **4.5:1**
- Large text: at least **3:1**

If something needs less emphasis, reduce its size, weight, or prominence before sacrificing readability.


### Spacing

Spacing also communicates hierarchy.

|Technique|Effect|
|---|---|
|Larger gap before a heading|Signals a new section|
|Small gap between label and value|Groups them together|
|Tighter line-height on large headings|Keeps large text visually cohesive|
|More generous line-height on paragraphs|Improves readability|

Useful starting ranges:

```
Body line-height:     1.4–1.6
Large heading:        1.1–1.3
Heading tracking:    -0.01em to -0.03em
Small all-caps:      +0.04em to +0.08em
```

These are starting points, not strict rules.


### Typeface & Style

Different type styles can communicate different roles.

```
Display serif   → expressive heading
Sans-serif      → normal UI/body content
Monospace       → code or technical data
Italic          → emphasis or citation
```

Keep those meanings consistent. If italics sometimes mean emphasis, sometimes product names, and sometimes quotes, the visual signal becomes less useful.


### Responsive Typography

Typography should respond to available space without destroying the hierarchy.

Instead of hard jumps:

```
font-size: 48px;
```

fluid sizing can use:

```
font-size: clamp(2rem, 4vw, 3rem);
```

This gives the text:

```
minimum size → fluid middle → maximum size
```

Use `rem` for the limits so browser text scaling still works.

For reusable components, container queries can adjust typography based on the component's own available width rather than the whole viewport.


### Semantic Hierarchy

Visual hierarchy and HTML structure should agree.

```
<h1>Page title</h1>
<h2>Section</h2>
<h3>Subsection</h3>
```

Do not choose `h1–h6` based on how large you want the text to look. Choose them based on document structure, then style them separately.


### Common Mistakes

- **Too many hierarchy levels.**  
    Several barely distinguishable levels make the interface harder to scan.
    
- **Using bold without enough size difference.**  
    Weight helps hierarchy, but usually should not carry it alone.
    
- **Making secondary text too faint.**  
    Lower priority should not mean difficult to read.
    
- **Using all-caps for long text.**  
    All-caps works better for short labels than paragraphs.
    
- **Creating hierarchy differently on every page.**  
    Reuse consistent type roles rather than inventing new combinations each time.