---
title: ParentNode
second_title: Aspose.Words for .NET API Reference
description: Node property. Gets the immediate parent of this node in C#.
type: docs
weight: 60
url: /net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Gets the immediate parent of this node.

```csharp
public CompositeNode ParentNode { get; }
```

## Remarks

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is `null`.

## Examples

Shows how to access a node's parent node.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Append a child Run node to the document's first paragraph.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// The paragraph is the parent node of the run node. We can trace this lineage
// all the way to the document node, which is the root of the document's node tree.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

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

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namespace [Aspose.Words](../../node/)
* assembly [Aspose.Words](../../../)
