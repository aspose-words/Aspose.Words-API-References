---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: Effortlessly clear your NodeCollection with our Clear method, removing all nodes from both the collection and the document for optimal performance.
type: docs
weight: 40
url: /net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Removes all nodes from this collection and from the document.

```csharp
public void Clear()
```

## Examples

Shows how to remove all sections from a document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// This document has one section with a few child nodes containing and displaying all the document's contents.
Assert.That(doc.Sections.Count, Is.EqualTo(1));
Assert.That(doc.Sections[0].GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(17));
Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello World!\r\rHello Word!\r\r\rHello World!"));

// Clear the collection of sections, which will remove all of the document's children.
doc.Sections.Clear();

Assert.That(doc.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(0));
Assert.That(doc.GetText().Trim(), Is.EqualTo(string.Empty));
```

### See Also

* class [NodeCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
