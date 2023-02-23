---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
second_title: Aspose.Words for .NET API Reference
description: Document method. If the document contains no sections creates one section with one paragraph in C#.
type: docs
weight: 580
url: /net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

If the document contains no sections, creates one section with one paragraph.

```csharp
public void EnsureMinimum()
```

## Examples

Shows how to ensure that a document contains the minimal set of nodes required for editing its contents.

```csharp
// A newly created document contains one child Section, which includes one child Body and one child Paragraph.
// We can edit the document body's contents by adding nodes such as Runs or inline Shapes to that paragraph.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// This is the minimal set of nodes that we need to be able to edit the document.
// We will no longer be able to edit the document if we remove any of them.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Call this method to make sure that the document has at least those three nodes so we can edit it again.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
