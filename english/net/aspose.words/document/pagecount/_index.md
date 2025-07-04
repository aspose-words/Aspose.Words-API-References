---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words for .NET
description: Discover the Document PageCount property, which reveals the total page count based on the latest layout, ensuring accurate document management and insights.
type: docs
weight: 330
url: /net/aspose.words/document/pagecount/
---
## Document.PageCount property

Gets the number of pages in the document as calculated by the most recent page layout operation.

```csharp
public int PageCount { get; }
```

## Examples

Shows how to count the number of pages in the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Verify the expected page count of the document.
Assert.That(doc.PageCount, Is.EqualTo(3));

// Getting the PageCount property invoked the document's page layout to calculate the value.
// This operation will not need to be re-done when rendering the document to a fixed page save format,
// such as .pdf. So you can save some time, especially with more complex documents.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### See Also

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
