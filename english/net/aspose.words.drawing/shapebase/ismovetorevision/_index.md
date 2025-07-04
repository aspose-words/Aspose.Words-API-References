---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words for .NET
description: Discover how ShapeBase's IsMoveToRevision property enhances your Microsoft Word experience by tracking object movements seamlessly during edits.
type: docs
weight: 350
url: /net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

Returns `true` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

```csharp
public bool IsMoveToRevision { get; }
```

## Examples

Shows how to identify move revision shapes.

```csharp
// A move revision is when we move an element in the document body by cut-and-pasting it in Microsoft Word while
// tracking changes. If we involve an inline shape in such a text movement, that shape will also be a revision.
// Copying-and-pasting or moving floating shapes do not create move revisions.
Document doc = new Document(MyDir + "Revision shape.docx");

// Move revisions consist of pairs of "Move from", and "Move to" revisions. We moved in this document in one shape,
// but until we accept or reject the move revision, there will be two instances of that shape.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.That(shapes.Length, Is.EqualTo(2));

// This is the "Move to" revision, which is the shape at its arrival destination.
// If we accept the revision, this "Move to" revision shape will disappear,
// and the "Move from" revision shape will remain.
Assert.That(shapes[0].IsMoveFromRevision, Is.False);
Assert.That(shapes[0].IsMoveToRevision, Is.True);

// This is the "Move from" revision, which is the shape at its original location.
// If we accept the revision, this "Move from" revision shape will disappear,
// and the "Move to" revision shape will remain.
Assert.That(shapes[1].IsMoveFromRevision, Is.True);
Assert.That(shapes[1].IsMoveToRevision, Is.False);
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
