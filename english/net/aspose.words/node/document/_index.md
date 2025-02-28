---
title: Node.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: Discover the Node Document property: effortlessly access the document linked to your node for seamless data management and enhanced productivity.
type: docs
weight: 20
url: /net/aspose.words/node/document/
---
## Node.Document property

Gets the document to which this node belongs.

```csharp
public virtual DocumentBase Document { get; }
```

## Remarks

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

## Examples

Shows how to create a node and set its owning document.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// We have not yet appended this paragraph as a child to any composite node.
Assert.IsNull(para.ParentNode);

// If a node is an appropriate child node type of another composite node,
// we can attach it as a child only if both nodes have the same owner document.
// The owner document is the document we passed to the node's constructor.
// We have not attached this paragraph to the document, so the document does not contain its text.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Add this node to the document, and then verify its contents.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### See Also

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
