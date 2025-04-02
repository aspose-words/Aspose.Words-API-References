---
title: BorderCollection.clearFormatting method
linktitle: clearFormatting method
articleTitle: clearFormatting method
second_title: Aspose.Words for NodeJs
description: "BorderCollection.clearFormatting method. Removes all borders of an object."
type: docs
weight: 150
url: /nodejs-net/Aspose.Words/bordercollection/clearFormatting/
---

## clearFormatting() {#default}

Removes all borders of an object.


```js
clearFormatting()
```

### Examples

Shows how to remove all borders from all paragraphs in a document.

```js
let doc = new aw.Document(base.myDir + "Borders.docx");

// The first paragraph of this document has visible borders with these settings.
let firstParagraphBorders = doc.firstSection.body.firstParagraph.paragraphFormat.borders;

expect(firstParagraphBorders.color).toEqual("#FF0000");
expect(firstParagraphBorders.lineStyle).toEqual(aw.LineStyle.Single);
expect(firstParagraphBorders.lineWidth).toEqual(3.0);

// Use the "ClearFormatting" method on each paragraph to remove all borders.
for (let paragraph of doc.firstSection.body.paragraphs.toArray()) {
  paragraph.paragraphFormat.borders.clearFormatting();

  for (let border of paragraph.paragraphFormat.borders) {
    expect(border.color).toEqual(base.emptyColor);
    expect(border.lineStyle).toEqual(aw.LineStyle.None);
    expect(border.lineWidth).toEqual(0.0);
  }
}

doc.save(base.artifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [BorderCollection](../)

