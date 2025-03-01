---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words for .NET
description: Discover the ShapeBase AnchorLocked property to control anchor locking for shapes, enhancing design stability and flexibility in your projects.
type: docs
weight: 30
url: /net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Specifies whether the shape's anchor is locked.

```csharp
public bool AnchorLocked { get; set; }
```

## Remarks

The default value is `false`.

Has effect only for top level shapes.

This property affects behavior of the shape's anchor in Microsoft Word. When the anchor is not locked, moving the shape in Microsoft Word can move the shape's anchor too.

## Examples

Shows how to lock or unlock a shape's paragraph anchor.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Set the "AnchorLocked" property to "true" to prevent the shape's anchor
// from moving when moving the shape in Microsoft Word.
// Set the "AnchorLocked" property to "false" to allow any movement of the shape
// to also move its anchor to any other paragraph that the shape ends up close to.
shape.AnchorLocked = anchorLocked;

// If the shape does not have a visible anchor symbol to its left,
// we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
