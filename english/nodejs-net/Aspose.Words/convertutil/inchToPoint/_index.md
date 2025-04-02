---
title: ConvertUtil.inchToPoint method
linktitle: inchToPoint method
articleTitle: inchToPoint method
second_title: Aspose.Words for NodeJs
description: "ConvertUtil.inchToPoint method. Converts inches to points."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/convertutil/inchToPoint/
---

## inchToPoint(inches) {#number}

Converts inches to points.


```js
inchToPoint(inches: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inches | number | The value to convert. |

### Remarks

1 inch equals 72 points.


### Examples

Shows how to specify page properties in inches.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A section's "Page Setup" defines the size of the page margins in points.
// We can also use the "ConvertUtil" class to use a more familiar measurement unit,
// such as inches when defining boundaries.
let pageSetup = builder.pageSetup;
pageSetup.topMargin = aw.ConvertUtil.inchToPoint(1.0);
pageSetup.bottomMargin = aw.ConvertUtil.inchToPoint(2.0);
pageSetup.leftMargin = aw.ConvertUtil.inchToPoint(2.5);
pageSetup.rightMargin = aw.ConvertUtil.inchToPoint(1.5);

// An inch is 72 points.
expect(aw.ConvertUtil.inchToPoint(1)).toEqual(72.0);
expect(aw.ConvertUtil.pointToInch(72)).toEqual(1.0);

// Add content to demonstrate the new margins.
builder.writeln(`This Text is ${pageSetup.leftMargin} points/${aw.ConvertUtil.pointToInch(pageSetup.leftMargin)} inches from the left, ` +
        `${pageSetup.rightMargin} points/${aw.ConvertUtil.pointToInch(pageSetup.rightMargin)} inches from the right, ` +
        `${pageSetup.topMargin} points/${aw.ConvertUtil.pointToInch(pageSetup.topMargin)} inches from the top, ` +
        `and ${pageSetup.bottomMargin} points/${aw.ConvertUtil.pointToInch(pageSetup.bottomMargin)} inches from the bottom of the page.`);

doc.save(base.artifactsDir + "UtilityClasses.PointsAndInches.docx");
```

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.pageSetup.paperSize = aw.PaperSize.Legal;
builder.pageSetup.orientation = aw.Orientation.Landscape;
builder.pageSetup.topMargin = aw.ConvertUtil.inchToPoint(1.0);
builder.pageSetup.bottomMargin = aw.ConvertUtil.inchToPoint(1.0);
builder.pageSetup.leftMargin = aw.ConvertUtil.inchToPoint(1.5);
builder.pageSetup.rightMargin = aw.ConvertUtil.inchToPoint(1.5);
builder.pageSetup.headerDistance = aw.ConvertUtil.inchToPoint(0.2);
builder.pageSetup.footerDistance = aw.ConvertUtil.inchToPoint(0.2);

builder.writeln("Hello world!");

doc.save(base.artifactsDir + "PageSetup.pageMargins.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ConvertUtil](../)

