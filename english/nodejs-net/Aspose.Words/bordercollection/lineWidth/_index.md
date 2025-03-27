---
title: BorderCollection.lineWidth property
linktitle: lineWidth property
articleTitle: lineWidth property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.lineWidth property. Gets or sets the border width in points."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words/bordercollection/lineWidth/
---

## BorderCollection.lineWidth property

Gets or sets the border width in points.


```js
get lineWidth(): number
```

### Remarks

Returns the width of the first border in the collection.

Sets the width of all borders in the collection excluding diagonal borders.




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

