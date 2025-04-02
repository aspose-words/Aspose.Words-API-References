---
title: BorderCollection.distanceFromText property
linktitle: distanceFromText property
articleTitle: distanceFromText property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.distanceFromText property. Gets or sets distance of the border from text in points."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/bordercollection/distanceFromText/
---

## BorderCollection.distanceFromText property

Gets or sets distance of the border from text in points.


```js
get distanceFromText(): number
```

### Remarks

Gets the distance from text for the first border.

Sets the distance from text for all borders in the collection excluding diagonal borders.

Has no effect and will be automatically reset to zero for borders of table cells.




### Examples

Shows how to create green wavy page border with a shadow.

```js
let doc = new aw.Document();
let pageSetup = doc.sections.at(0).pageSetup;

pageSetup.borders.lineStyle = aw.LineStyle.DoubleWave;
pageSetup.borders.lineWidth = 2;
pageSetup.borders.color = "#008000";
pageSetup.borders.distanceFromText = 24;
pageSetup.borders.shadow = true;

doc.save(base.artifactsDir + "PageSetup.PageBorders.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [BorderCollection](../)

