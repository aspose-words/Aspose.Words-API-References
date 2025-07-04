---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words for .NET
description: Discover the ShapeBase IsDeleteRevision property, learn how it indicates object deletion in Microsoft Word with change tracking enabled for enhanced document management.
type: docs
weight: 270
url: /net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

```csharp
public bool IsDeleteRevision { get; }
```

## Examples

Shows how to work with revision shapes.

```csharp
Document doc = new Document();

Assert.That(doc.TrackRevisions, Is.False);

// Insert an inline shape without tracking revisions, which will make this shape not a revision of any kind.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Start tracking revisions and then insert another shape, which will be a revision.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.That(shapes.Length, Is.EqualTo(2));

shapes[0].Remove();

// Since we removed that shape while we were tracking changes,
// the shape persists in the document and counts as a delete revision.
// Accepting this revision will remove the shape permanently, and rejecting it will keep it in the document.
Assert.That(shapes[0].ShapeType, Is.EqualTo(ShapeType.Cube));
Assert.That(shapes[0].IsDeleteRevision, Is.True);

// And we inserted another shape while tracking changes, so that shape will count as an insert revision.
// Accepting this revision will assimilate this shape into the document as a non-revision,
// and rejecting the revision will remove this shape permanently.
Assert.That(shapes[1].ShapeType, Is.EqualTo(ShapeType.Sun));
Assert.That(shapes[1].IsInsertRevision, Is.True);
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
