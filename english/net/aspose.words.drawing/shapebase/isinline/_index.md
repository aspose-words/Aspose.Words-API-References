---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words for .NET
description: Discover the ShapeBase IsInline property to easily check if your shape aligns with text, enhancing your design and improving layout efficiency.
type: docs
weight: 310
url: /net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

A quick way to determine if this shape is positioned inline with text.

```csharp
public bool IsInline { get; }
```

## Remarks

Has effect only for top level shapes.

## Examples

Shows how to determine whether a shape is inline or floating.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two wrapping types that shapes may have.
// 1 -  Inline:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// An inline shape sits inside a paragraph among other paragraph elements, such as runs of text.
// In Microsoft Word, we may click and drag the shape to any paragraph as if it is a character.
// If the shape is large, it will affect vertical paragraph spacing.
// We cannot move this shape to a place with no paragraph.
Assert.That(shape.WrapType, Is.EqualTo(WrapType.Inline));
Assert.That(shape.IsInline, Is.True);

// 2 -  Floating:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// A floating shape belongs to the paragraph that we insert it into,
// which we can determine by an anchor symbol that appears when we click the shape.
// If the shape does not have a visible anchor symbol to its left,
// we will need to enable visible anchors via "Options" -> "Display" -> "Object Anchors".
// In Microsoft Word, we may left click and drag this shape freely to any location.
Assert.That(shape.WrapType, Is.EqualTo(WrapType.None));
Assert.That(shape.IsInline, Is.False);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
