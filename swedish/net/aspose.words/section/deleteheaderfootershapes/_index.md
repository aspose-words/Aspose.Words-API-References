---
title: Section.DeleteHeaderFooterShapes
linktitle: DeleteHeaderFooterShapes
articleTitle: DeleteHeaderFooterShapes
second_title: Aspose.Words för .NET
description: Section DeleteHeaderFooterShapes metod. Tar bort alla former ritobjekt från sidhuvuden och sidfötter i det här avsnittet i C#.
type: docs
weight: 120
url: /sv/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

Tar bort alla former (ritobjekt) från sidhuvuden och sidfötter i det här avsnittet.

```csharp
public void DeleteHeaderFooterShapes()
```

## Exempel

Visar hur du tar bort alla former från alla sidhuvuden och sidfötter i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en primär rubrik med en form.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// Skapa en primär sidfot med en bild.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo Icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// Ta bort alla former från sidhuvuden och sidfötter i det första avsnittet.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
