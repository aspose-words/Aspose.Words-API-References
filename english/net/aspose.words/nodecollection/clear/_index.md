---
title: NodeCollection.Clear
linktitle: Clear
second_title: Aspose.Words for .NET API Reference
description: NodeCollection Clear method. Removes all nodes from this collection and from the document in C#.
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
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Clear the collection of sections, which will remove all of the document's children.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### See Also

* class [NodeCollection](../)
* namespace [Aspose.Words](../../nodecollection/)
* assembly [Aspose.Words](../../../)
