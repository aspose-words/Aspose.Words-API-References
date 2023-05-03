---
title: LayoutCollector
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words for .NET API Reference
description: LayoutCollector constructor. Initializes an instance of this class in C#.
type: docs
weight: 10
url: /net/aspose.words.layout/layoutcollector/layoutcollector/
---
## LayoutCollector constructor

Initializes an instance of this class.

```csharp
public LayoutCollector(Document doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | Document | The document to which this collector instance will be attached to. |

## Examples

Shows how to see the the ranges of pages that a node spans.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
// Since the document is empty, that number of pages is currently zero.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Populate the document with 5 pages of content.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Before the layout collector, we need to call the "UpdatePageLayout" method to give us
// an accurate figure for any layout-related metric, such as the page count.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// We can see the numbers of the start and end pages of any node and their overall page spans.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// We can iterate over the layout entities using a LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// The LayoutEnumerator can traverse the collection of layout entities like a tree.
// We can also apply it to any node's corresponding layout entity.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [LayoutCollector](../)
* namespace [Aspose.Words.Layout](../../layoutcollector/)
* assembly [Aspose.Words](../../../)
