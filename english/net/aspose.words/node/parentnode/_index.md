---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words for .NET
description: Discover the Node ParentNode property to easily access the immediate parent of any node, enhancing your web development efficiency and code clarity.
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
Assert.That(run.ParentNode, Is.EqualTo(para));
Assert.That(para.ParentNode, Is.EqualTo(doc.FirstSection.Body));
Assert.That(doc.FirstSection.Body.ParentNode, Is.EqualTo(doc.FirstSection));
Assert.That(doc.FirstSection.ParentNode, Is.EqualTo(doc));
```

Shows how to create a node and set its owning document.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// We have not yet appended this paragraph as a child to any composite node.
Assert.That(para.ParentNode, Is.Null);

// If a node is an appropriate child node type of another composite node,
// we can attach it as a child only if both nodes have the same owner document.
// The owner document is the document we passed to the node's constructor.
// We have not attached this paragraph to the document, so the document does not contain its text.
Assert.That(doc, Is.EqualTo(para.Document));
Assert.That(doc.GetText().Trim(), Is.EqualTo(string.Empty));

// Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Add this node to the document, and then verify its contents.
doc.FirstSection.Body.AppendChild(para);

Assert.That(para.ParentNode, Is.EqualTo(doc.FirstSection.Body));
Assert.That(doc.GetText().Trim(), Is.EqualTo("Hello world!"));
```

### See Also

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
