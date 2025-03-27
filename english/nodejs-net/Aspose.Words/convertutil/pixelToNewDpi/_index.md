---
title: ConvertUtil.pixelToNewDpi method
linktitle: pixelToNewDpi method
articleTitle: pixelToNewDpi method
second_title: Aspose.Words for NodeJs
description: "ConvertUtil.pixelToNewDpi method. Converts pixels from one resolution to another."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words/convertutil/pixelToNewDpi/
---

## pixelToNewDpi(pixels, oldDpi, newDpi) {#number_number_number}

Converts pixels from one resolution to another.


```js
pixelToNewDpi(pixels: numberoldDpi: numbernewDpi: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pixels | number | The value to convert. |
| oldDpi | number | The current dpi (dots per inch) resolution. |
| newDpi | number | The new dpi (dots per inch) resolution. |

### Examples

Shows how to use convert points to pixels with default and custom resolution.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Define the size of the top margin of this section in pixels, according to a custom DPI.
const myDpi = 192;

let pageSetup = builder.pageSetup;
pageSetup.topMargin = aw.ConvertUtil.pixelToPoint(100, myDpi);

expect(pageSetup.topMargin).toBeCloseTo(37.5, 2);

// At the default DPI of 96, a pixel is 0.75 points.
expect(aw.ConvertUtil.pixelToPoint(1)).toEqual(0.75);

builder.writeln(`This Text is ${pageSetup.topMargin} points/${aw.ConvertUtil.pointToPixel(pageSetup.topMargin, myDpi)} ` +
        `pixels (at a DPI of ${myDpi}) from the top of the page.`);

// Set a new DPI and adjust the top margin value accordingly.
const newDpi = 300;
pageSetup.topMargin = aw.ConvertUtil.pixelToNewDpi(pageSetup.topMargin, myDpi, newDpi);
expect(pageSetup.topMargin).toBeCloseTo(59.0, 2);

builder.writeln(`At a DPI of ${newDpi}, the text is now ${pageSetup.topMargin} points/${aw.ConvertUtil.pointToPixel(pageSetup.topMargin, myDpi)} ` +
        "pixels from the top of the page.");

doc.save(base.artifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ConvertUtil](../)

