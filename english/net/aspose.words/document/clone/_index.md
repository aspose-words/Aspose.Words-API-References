---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Effortlessly duplicate your documents with our Document Clone method. Achieve precise deep copies for seamless editing and efficient workflow.
type: docs
weight: 590
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

Assert.That(clone.FirstSection.Body.FirstParagraph.Runs[0].Text, Is.EqualTo(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText()));
Assert.That(clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(), Is.Not.EqualTo(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode()));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
