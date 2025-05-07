---
title: ShapeBase.isInline property
linktitle: isInline property
articleTitle: isInline property
second_title: Aspose.Words for Node.js
description: "ShapeBase.isInline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 260
url: /nodejs-net/aspose.words.drawing/shapebase/isInline/
---

## ShapeBase.isInline property

A quick way to determine if this shape is positioned inline with text.


```js
get isInline(): boolean
```

### Remarks

Has effect only for top level shapes.




### Examples

Shows how to determine whether a shape is inline or floating.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Inline:
builder.write("Hello world! ");
let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, 100, 100);
shape.fillColor = "#ADD8E6";
builder.write(" Hello again.");

// An inline shape sits inside a paragraph among other paragraph elements, such as runs of text.
// In Microsoft Word, we may click and drag the shape to any paragraph as if it is a character.
// If the shape is large, it will affect vertical paragraph spacing.
// We cannot move this shape to a place with no paragraph.
expect(shape.wrapType).toEqual(aw.Drawing.WrapType.Inline);
expect(shape.isInline).toEqual(true);

// 2 -  Floating:
shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 200,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 200, 100, 100, aw.Drawing.WrapType.None);
shape.fillColor = "#FFA500";

// A floating shape belongs to the paragraph that we insert it into,
// which we can determine by an anchor symbol that appears when we click the shape.
// If the shape does not have a visible anchor symbol to its left,
// we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
// In Microsoft Word, we may left click and drag this shape freely to any location.
expect(shape.wrapType).toEqual(aw.Drawing.WrapType.None);
expect(shape.isInline).toEqual(false);

doc.save(base.artifactsDir + "Shape.isInline.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

