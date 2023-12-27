---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Document Clone method. Performs a deep copy of the Document in C#.
type: docs
weight: 580
url: /net/aspose.words/document/clone/
---
## Document.Clone method

Performs a deep copy of the [`Document`](../).

```csharp
public Document Clone()
```

### Return Value

The cloned document.

## Examples

Shows how to deep clone a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// Cloning will produce a new document with the same contents as the original,
// but with a unique copy of each of the original document's nodes.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
