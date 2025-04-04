---
title: ConvertUtil.millimeterToPoint method
linktitle: millimeterToPoint method
articleTitle: millimeterToPoint method
second_title: Aspose.Words for Node.js
description: "ConvertUtil.millimeterToPoint method. Converts millimeters to points."
type: docs
weight: 20
url: /nodejs-net/aspose.words/convertutil/millimeterToPoint/
---

## millimeterToPoint(millimeters) {#number}

Converts millimeters to points.


```js
millimeterToPoint(millimeters: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | number | The value to convert. |

### Remarks

1 inch equals 25.4 millimeters. 1 inch equals 72 points.


### Examples

Shows how to specify page properties in millimeters.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A section's "Page Setup" defines the size of the page margins in points.
// We can also use the "ConvertUtil" class to use a more familiar measurement unit,
// such as millimeters when defining boundaries.
let pageSetup = builder.pageSetup;
pageSetup.topMargin = aw.ConvertUtil.millimeterToPoint(30);
pageSetup.bottomMargin = aw.ConvertUtil.millimeterToPoint(50);
pageSetup.leftMargin = aw.ConvertUtil.millimeterToPoint(80);
pageSetup.rightMargin = aw.ConvertUtil.millimeterToPoint(40);

// A centimeter is approximately 28.3 points.
expect(aw.ConvertUtil.millimeterToPoint(10)).toBeCloseTo(28.34, 1);

// Add content to demonstrate the new margins.
builder.writeln(`This Text is ${pageSetup.leftMargin} points from the left, ` +
        `${pageSetup.rightMargin} points from the right, ` +
        `${pageSetup.topMargin} points from the top, ` +
        `and ${pageSetup.bottomMargin} points from the bottom of the page.`);

doc.save(base.artifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ConvertUtil](../)

