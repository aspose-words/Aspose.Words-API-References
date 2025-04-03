---
title: ShapeBase.anchorLocked property
linktitle: anchorLocked property
articleTitle: anchorLocked property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.anchorLocked property. Specifies whether the shape's anchor is locked."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Drawing/shapebase/anchorLocked/
---

## ShapeBase.anchorLocked property

Specifies whether the shape's anchor is locked.


```js
get anchorLocked(): boolean
```

### Remarks

The default value is ``false``.

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word.
When the anchor is not locked, moving the shape in Microsoft Word can move
the shape's anchor too.




### Examples

Shows how to lock or unlock a shape's paragraph anchor.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");

builder.write("Our shape will have an anchor attached to this paragraph.");
let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, 200, 160);
shape.wrapType = aw.Drawing.WrapType.None;
builder.insertBreak(aw.BreakType.ParagraphBreak);

builder.writeln("Hello again!");

// Set the "AnchorLocked" property to "true" to prevent the shape's anchor
// from moving when moving the shape in Microsoft Word.
// Set the "AnchorLocked" property to "false" to allow any movement of the shape
// to also move its anchor to any other paragraph that the shape ends up close to.
shape.anchorLocked = anchorLocked;

// If the shape does not have a visible anchor symbol to its left,
// we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
doc.save(base.artifactsDir + "Shape.anchorLocked.docx");
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

