---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words for .NET API Reference
description: LayoutCollector GetEntity method. Returns an opaque position of the LayoutEnumerator which corresponds to the specified node. You can use returned value as an argument to Current given the document being enumerated and the document of the node are the same in C#.
type: docs
weight: 50
url: /net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Returns an opaque position of the [`LayoutEnumerator`](../../layoutenumerator/) which corresponds to the specified node. You can use returned value as an argument to [`Current`](../../layoutenumerator/current/) given the document being enumerated and the document of the node are the same.

```csharp
public object GetEntity(Node node)
```

## Remarks

This method works for only [`Paragraph`](../../../aspose.words/paragraph/) nodes, as well as indivisible inline nodes, e.g. [`BookmarkStart`](../../../aspose.words/bookmarkstart/) or [`Shape`](../../../aspose.words.drawing/shape/). It doesn't work for [`Run`](../../../aspose.words/run/), [`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) or [`Table`](../../../aspose.words.tables/table/) nodes, and nodes within header/footer.

Note that the entity returned for a [`Paragraph`](../../../aspose.words/paragraph/) node is a paragraph break span. Use the appropriate method to ascend to the parent line

If you need to navigate to a [`Run`](../../../aspose.words/run/) of text then you can insert bookmark right before it and then navigate to the bookmark instead.

If you need to navigate to a [`Cell`](../../../aspose.words.tables/cell/) node then you can move to a [`Paragraph`](../../../aspose.words/paragraph/) node in this cell and then ascend to a parent entity. The same approach can be used for [`Row`](../../../aspose.words.tables/row/) and [`Table`](../../../aspose.words.tables/table/) nodes.

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* namespace [Aspose.Words.Layout](../../layoutcollector/)
* assembly [Aspose.Words](../../../)
