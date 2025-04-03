---
title: BorderCollection.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for NodeJs
description: "BorderCollection.equals method. Compares collections of borders."
type: docs
weight: 160
url: /nodejs-net/aspose.words/bordercollection/equals/
---

## equals(brColl) {#bordercollection}

Compares collections of borders.


```js
equals(brColl: Aspose.Words.BorderCollection)
```

| Parameter | Type | Description |
| --- | --- | --- |
| brColl | [BorderCollection](../) |  |

### Examples

Shows how border collections can share elements.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Paragraph 1.");
builder.write("Paragraph 2.");

// Since we used the same border configuration while creating
// these paragraphs, their border collections share the same elements.
let firstParagraphBorders = doc.firstSection.body.firstParagraph.paragraphFormat.borders;
let secondParagraphBorders = builder.currentParagraph.paragraphFormat.borders;
expect(firstParagraphBorders.count).toEqual(6);

for (let i = 0; i < firstParagraphBorders.count; i++)
{
  expect(firstParagraphBorders.at(i).equals(secondParagraphBorders.at(i))).toEqual(true);
  expect(firstParagraphBorders.at(i).isVisible).toEqual(false);
}

for (let border of secondParagraphBorders)
  border.lineStyle = aw.LineStyle.DotDash;

// After changing the line style of the borders in just the second paragraph,
// the border collections no longer share the same elements.
for (let i = 0; i < firstParagraphBorders.count; i++)
{
  expect(firstParagraphBorders.at(i).equals(secondParagraphBorders.at(i))).toEqual(false);

  // Changing the appearance of an empty border makes it visible.
  expect(secondParagraphBorders.at(i).isVisible).toEqual(true);
}

doc.save(base.artifactsDir + "Border.SharedElements.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [BorderCollection](../)

