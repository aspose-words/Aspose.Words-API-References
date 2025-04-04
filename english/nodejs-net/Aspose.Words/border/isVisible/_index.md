---
title: Border.isVisible property
linktitle: isVisible property
articleTitle: isVisible property
second_title: Aspose.Words for Node.js
description: "Border.isVisible property. Returns ``true`` if the [Border.lineStyle](../lineStyle/) is not [LineStyle.None](../../linestyle/#None)."
type: docs
weight: 30
url: /nodejs-net/aspose.words/border/isVisible/
---

## Border.isVisible property

Returns ``true`` if the [Border.lineStyle](../lineStyle/) is not [LineStyle.None](../../linestyle/#None).



```js
get isVisible(): boolean
```

### Examples

Shows how to remove borders from a paragraph.

```js
let doc = new aw.Document(base.myDir + "Borders.docx");

// Each paragraph has an individual set of borders.
// We can access the settings for the appearance of these borders via the paragraph format object.
let borders = doc.firstSection.body.firstParagraph.paragraphFormat.borders;

expect(borders.at(0).color).toEqual("#FF0000");
expect(borders.at(0).lineWidth).toEqual(3.0);
expect(borders.at(0).lineStyle).toEqual(aw.LineStyle.Single);
expect(borders.at(0).isVisible).toEqual(true);

// We can remove a border at once by running the ClearFormatting method. 
// Running this method on every border of a paragraph will remove all its borders.
//[...borders].forEach((b) => b.clearFormatting());
for (let b of borders)
  b.clearFormatting();

expect(borders.at(0).color).toEqual(base.emptyColor);
expect(borders.at(0).lineWidth).toEqual(0.0);
expect(borders.at(0).lineStyle).toEqual(aw.LineStyle.None);
expect(borders.at(0).isVisible).toEqual(false);

doc.save(base.artifactsDir + "Border.clearFormatting.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Border](../)

