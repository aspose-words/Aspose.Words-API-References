---
title: LayoutCollector.GetStartPageIndex
linktitle: GetStartPageIndex
articleTitle: GetStartPageIndex
second_title: Aspose.Words for .NET
description: Discover the LayoutCollector GetStartPageIndex method to easily find the 1-based index of a node's starting page. Simplify your mapping process today!
type: docs
weight: 70
url: /net/aspose.words.layout/layoutcollector/getstartpageindex/
---
## LayoutCollector.GetStartPageIndex method

Gets 1-based index of the page where node begins. Returns 0 if node cannot be mapped to a page.

```csharp
public int GetStartPageIndex(Node node)
```

## Examples

Shows how to see the the ranges of pages that a node spans.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
// Since the document is empty, that number of pages is currently zero.
Assert.That(layoutCollector.Document, Is.EqualTo(doc));
Assert.That(layoutCollector.GetNumPagesSpanned(doc), Is.EqualTo(0));

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
Assert.That(layoutCollector.GetNumPagesSpanned(doc), Is.EqualTo(0));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.That(layoutCollector.GetNumPagesSpanned(doc), Is.EqualTo(5));

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

Assert.That(layoutEnumerator.Type, Is.EqualTo(LayoutEntityType.Page));

// The LayoutEnumerator can traverse the collection of layout entities like a tree.
// We can also apply it to any node's corresponding layout entity.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.That(layoutEnumerator.Type, Is.EqualTo(LayoutEntityType.Span));
Assert.That(layoutEnumerator.Text, Is.EqualTo("¶"));
```

### See Also

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
