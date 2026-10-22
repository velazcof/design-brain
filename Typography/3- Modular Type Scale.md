
A modular type scale is a **small set of font sizes generated from one base size and a consistent ratio**.

✔️ A good type scale creates predictable hierarchy and removes random sizing decisions.

❌ A bad one mixes arbitrary values like `15px`, `17px`, `22px`, and `31px` with no relationship between them.


### How It Works

Start with a base size, usually `1rem`, then multiply or divide it by the same ratio.

Example using a `1.25` ratio:

```
0.80rem
1.00rem
1.25rem
1.56rem
1.95rem
2.44rem
```

Each step is `1.25×` the previous one, so the differences between sizes stay proportional.


### Common Ratios

|Ratio|Feel|Typical Use|
|---|---|---|
|**1.125**|Subtle|Reading-heavy layouts|
|**1.20**|Moderate|Product UI, dashboards|
|**1.25**|Balanced|General-purpose interfaces|
|**1.333**|Expansive|Portfolios, landing pages|
|**1.5+**|Dramatic|Display-heavy typography|

You do not need to use every generated step. Most interfaces only need a small subset for body text, headings, labels, and display text.


### Base Size

`1rem` is a common starting point for body text.

Use `rem` rather than fixed `px` values so typography can respect browser font-size preferences.


### From Scale to Roles

Raw scale values should eventually map to meaningful roles:

```
--text-base: 1rem;
--text-lg: 1.25rem;
--text-xl: 1.56rem;
```

Then:

```
--font-body: var(--text-base);
--font-heading-2: var(--text-xl);
```

This keeps component styles tied to **purpose**, not arbitrary numbers.


### Fluid Type

A type scale can also grow smoothly with the viewport using `clamp()`:

```
font-size: clamp(2rem, 1.2rem + 3vw, 3rem);
```

This means:

> Never smaller than `2rem`, grow fluidly in between, and never exceed `3rem`.

Use `rem` for the minimum and maximum so zoom and user font preferences still work properly.


### Common Mistakes

- **Using every generated step.**  
    Keep only the sizes that correspond to real interface roles.
    
- **Mixing magic numbers into the scale.**  
    A random `17px` value defeats the point of having a system.
    
- **Using the same dramatic ratio everywhere.**  
    Dense UIs usually need tighter scales than marketing or portfolio pages.
    
- **Hardcoding typography per component.**  
    Reuse named size roles instead.