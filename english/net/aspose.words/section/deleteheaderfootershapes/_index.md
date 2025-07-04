---
title: Section.DeleteHeaderFooterShapes
linktitle: DeleteHeaderFooterShapes
articleTitle: DeleteHeaderFooterShapes
second_title: Aspose.Words for .NET
description: Effortlessly remove all drawing shapes from section headers and footers with the DeleteHeaderFooterShapes method for cleaner document presentation.
type: docs
weight: 140
url: /net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

Deletes all shapes (drawing objects) from the headers and footers of this section.

```csharp
public void DeleteHeaderFooterShapes()
```

## Examples

Shows how to remove all shapes from all headers footers in a section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a primary header with a shape.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// Create a primary footer with an image.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo icon.ico");

Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(1));
Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(1));

// Remove all shapes from the headers and footers in the first section.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(0));
Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(0));
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
