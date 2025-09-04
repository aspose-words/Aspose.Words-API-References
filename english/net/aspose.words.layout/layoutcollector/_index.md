---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Layout.LayoutCollector class to efficiently compute document node page numbers, enhancing your document management experience.
type: docs
weight: 3780
url: /net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

This class allows to compute page numbers of document nodes.

To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) documentation article.

```csharp
public class LayoutCollector
```

## Constructors

| Name | Description |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | Initializes an instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Gets or sets the document this collector instance is attached to. |

## Methods

| Name | Description |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Gets 1-based index of the page where node ends. Returns 0 if node cannot be mapped to a page. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Returns an opaque position of the [`LayoutEnumerator`](../layoutenumerator/) which corresponds to the specified node. You can use returned value as an argument to [`Current`](../layoutenumerator/current/) given the document being enumerated and the document of the node are the same. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Gets number of pages the specified node spans. 0 if node is within a single page. This is the same as [`GetEndPageIndex`](./getendpageindex/) - [`GetStartPageIndex`](./getstartpageindex/). |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Gets 1-based index of the page where node begins. Returns 0 if node cannot be mapped to a page. |

## Remarks

When you create a `LayoutCollector` and specify a [`Document`](../../aspose.words/document/) document object to attach to, the collector will record mapping of document nodes to layout objects when the document is formatted into pages.

You will be able to find out on which page a particular document node (e.g. run, paragraph or table cell) is located by using the [`GetStartPageIndex`](./getstartpageindex/), [`GetEndPageIndex`](./getendpageindex/) and [`GetNumPagesSpanned`](./getnumpagesspanned/) methods. These methods automatically build page layout model of the document and update fields if required.

When you no longer need to collect layout information, it is best to set the [`Document`](./document/) property to `null` to avoid unnecessary collection of more layout mappings.

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

* namespace [Aspose.Words.Layout](../../aspose.words.layout/)
* assembly [Aspose.Words](../../)
