---
title: BorderCollection.lineStyle property
linktitle: lineStyle property
articleTitle: lineStyle property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.lineStyle property. Gets or sets the border style."
type: docs
weight: 70
url: /nodejs-net/aspose.words/bordercollection/lineStyle/
---

## BorderCollection.lineStyle property

Gets or sets the border style.


```js
get lineStyle(): Aspose.Words.LineStyle
```

### Remarks

Returns the style of the first border in the collection.

Sets the style of all borders in the collection excluding diagonal borders.




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

