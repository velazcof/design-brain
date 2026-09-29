
A reference for common screen, resolution, viewport, and responsive-design terms.

| Term                         | Meaning                                                                                | Example                                                         |
| ---------------------------- | -------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| **Screen Size**              | The physical size of a display, usually measured diagonally in inches.                 | 6.1" phone, 14" laptop, 27" monitor                             |
| **Resolution**               | The number of physical pixels in a display or image, written as width × height.        | `1920 × 1080`                                                   |
| **1080p**                    | A common resolution class with 1080 vertical pixels, usually `1920 × 1080`.            | Full HD monitor                                                 |
| **1440p**                    | Usually `2560 × 1440`.                                                                 | QHD monitor                                                     |
| **4K / UHD**                 | Usually `3840 × 2160` for consumer displays.                                           | 4K monitor or TV                                                |
| **Aspect Ratio**             | The proportional relationship between width and height.                                | `16:9`, `4:3`, `21:9`                                           |
| **Viewport**                 | The area of the browser currently available to display a webpage.                      | A page may have a `1440 × 850` CSS viewport on a larger monitor |
| **CSS Pixel**                | A logical pixel used by CSS. It does not necessarily map to one physical screen pixel. | `width: 300px`                                                  |
| **Physical Pixel**           | An actual hardware pixel on the display.                                               | A phone may physically be 1170px wide                           |
| **Device Pixel Ratio (DPR)** | Roughly how many physical pixels correspond to one CSS pixel in each dimension.        | `DPR 3`: a 1170px-wide screen may expose a 390px CSS viewport   |
| **Breakpoint**               | A width where the layout changes.                                                      | Switch navigation layout below `700px`                          |
| **Media Query**              | CSS that responds to viewport or device characteristics.                               | `@media (max-width: 700px)`                                     |
| **Container Query**          | CSS that responds to the available size of a component's container.                    | `@container (min-width: 500px)`                                 |
| **Responsive Design**        | Designing interfaces that adapt to different available sizes.                          | Cards changing from side-by-side to stacked                     |
| **Viewport Width (vw)**      | A unit relative to viewport width. `100vw` equals the viewport's full width.           | `width: 100vw`                                                  |
| **Viewport Height (vh)**     | A unit relative to viewport height. `100vh` equals the viewport's full height.         | `min-height: 100vh`                                             |
| **Pixel Density**            | How tightly physical pixels are packed into a given physical area.                     | High-density phone screens                                      |
| **PPI**                      | Pixels per inch — a measurement of display pixel density.                              | A phone usually has a much higher PPI than a desktop monitor    |


## Common Resolution Names

|Name|Typical Resolution|Aspect Ratio|
|---|---|---|
|**720p / HD**|1280 × 720|16:9|
|**1080p / Full HD**|1920 × 1080|16:9|
|**1440p / QHD**|2560 × 1440|16:9|
|**4K / UHD**|3840 × 2160|16:9|



## Common Aspect Ratios

|Ratio|Common Use|
|---|---|
|**16:9**|TVs, monitors, video|
|**16:10**|Modern laptops|
|**4:3**|Older monitors, tablets, older media|
|**21:9**|Ultrawide monitors|
|**~19.5:9**|Modern phones|
Aspect ratio describes **shape**, not resolution. 

For example: ```1920 × 1080 and 3840 × 2160``` are both `16:9`.



## Rough CSS Viewport Widths

| Device Type | Rough Width |
| ----------- | ----------- |
| **Phone**   | 320–480px   |
| **Tablet**  | 600–1000px  |
| **Laptop**  | 1200–1600px |
| **Desktop** | 1440px+     |
Common values: ```360, 375, 390, 412, 430, 768, 1024, 1280, 1366, 1440, 1536, 1920```

Any of these values should not automatically become breakpoints - choose breakpoints where the **content or layout actually stops working well**.

Examples:

- Navigation no longer fits horizontally
- Cards become too narrow
- Paragraph lines become too long
- Sidebar competes with the main content
- Two-column content should stack



## CSS Pixels vs Physical Pixels

A modern high-density phone might have:

```
Physical resolution: 1170 × 2532
CSS viewport width: 390px
DPR: 3
```

Roughly:

```
1170 / 3 = 390
```

The browser gives CSS a logical coordinate system so UI elements do not become microscopic on high-density screens, therefore, frontend development usually cares more about **CSS viewport/container width** than the display's physical resolution.