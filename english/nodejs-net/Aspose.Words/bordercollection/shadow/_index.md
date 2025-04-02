---
title: BorderCollection.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for NodeJs
description: "BorderCollection.shadow property. Gets or sets a value indicating whether the border has a shadow."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words/bordercollection/shadow/
---

## BorderCollection.shadow property

Gets or sets a value indicating whether the border has a shadow.


```js
get shadow(): boolean
```

### Remarks

Gets the value from the first border in the collection.

Sets the value for all borders in the collection excluding diagonal borders.




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

