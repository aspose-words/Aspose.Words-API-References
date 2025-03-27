---
title: BorderCollection.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.color property. Gets or sets the border color."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/bordercollection/color/
---

## BorderCollection.color property

Gets or sets the border color.


```js
get color(): string
```

### Remarks

Returns the color of the first border in the collection.

Sets the color of all borders in the collection excluding diagonal borders.




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

