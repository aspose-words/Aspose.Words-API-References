---
title: LayoutCollector class
linktitle: LayoutCollector class
articleTitle: LayoutCollector class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Layout.LayoutCollector class. This class allows to compute page numbers of document nodes."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Layout/layoutcollector/
---

## LayoutCollector class

This class allows to compute page numbers of document nodes.

To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/nodejs-net/converting-to-fixed-page-format/) documentation article.




### Remarks

When you create a [LayoutCollector](./) and specify a [Document](../../aspose.words/document/) document object to attach to, 
the collector will record mapping of document nodes to layout objects when the document is formatted into pages.

You will be able to find out on which page a particular document node (e.g. run, paragraph or table cell) is located
by using the [LayoutCollector.getStartPageIndex()](./getStartPageIndex/#node), [LayoutCollector.getEndPageIndex()](./getEndPageIndex/#node) and [LayoutCollector.getNumPagesSpanned()](./getNumPagesSpanned/#node) methods. 
These methods automatically build page layout model of the document and update fields if required.

When you no longer need to collect layout information, it is best to set the [LayoutCollector.document](./document/) property to ``null``
to avoid unnecessary collection of more layout mappings.




### Constructors
| Name | Description |
| --- | --- |
| [LayoutCollector(doc)](./constructor/#document) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets or sets the document this collector instance is attached to. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt. |
|[ getEndPageIndex(node)](./getEndPageIndex/#node) | Gets 1-based index of the page where node ends. Returns 0 if node cannot be mapped to a page. |
|[ getNumPagesSpanned(node)](./getNumPagesSpanned/#node) | Gets number of pages the specified node spans. 0 if node is within a single page. This is the same as [LayoutCollector.getEndPageIndex()](./getEndPageIndex/#node) - [LayoutCollector.getStartPageIndex()](./getStartPageIndex/#node). |
|[ getStartPageIndex(node)](./getStartPageIndex/#node) | Gets 1-based index of the page where node begins. Returns 0 if node cannot be mapped to a page. |

### Examples

Shows how to see the the ranges of pages that a node spans.

```js
let doc = new aw.Document();
let layoutCollector = new aw.Layout.LayoutCollector(doc);

// Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
// Since the document is empty, that number of pages is currently zero.
expect(layoutCollector.document).toEqual(doc);
expect(layoutCollector.getNumPagesSpanned(doc)).toEqual(0);

// Populate the document with 5 pages of content.
let builder = new aw.DocumentBuilder(doc);
builder.write("Section 1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.insertBreak(aw.BreakType.PageBreak);
builder.insertBreak(aw.BreakType.SectionBreakEvenPage);
builder.write("Section 2");
builder.insertBreak(aw.BreakType.PageBreak);
builder.insertBreak(aw.BreakType.PageBreak);

// Before the layout collector, we need to call the "UpdatePageLayout" method to give us
// an accurate figure for any layout-related metric, such as the page count.
expect(layoutCollector.getNumPagesSpanned(doc)).toEqual(0);

layoutCollector.clear();
doc.updatePageLayout();

expect(layoutCollector.getNumPagesSpanned(doc)).toEqual(5);

// We can see the numbers of the start and end pages of any node and their overall page spans.
let nodes = doc.getChildNodes(aw.NodeType.Any, true);
for (let node of nodes)
{
  console.log(`->  NodeType.${node.nodeType}: `);
  console.log(
    `\tStarts on page ${layoutCollector.getStartPageIndex(node)}, ends on page ${layoutCollector.getEndPageIndex(node)},` +
    ` spanning ${layoutCollector.getNumPagesSpanned(node)} pages.`);
}

// We can iterate over the layout entities using a LayoutEnumerator.
let layoutEnumerator = new aw.Layout.LayoutEnumerator(doc);

expect(layoutEnumerator.type).toEqual(aw.Layout.LayoutEntityType.Page);

// The LayoutEnumerator can traverse the collection of layout entities like a tree.
// We can also apply it to any node's corresponding layout entity.
layoutEnumerator.current = layoutCollector.getEntity(doc.getChild(aw.NodeType.Paragraph, 1, true));

expect(layoutEnumerator.type).toEqual(aw.Layout.LayoutEntityType.Span);
expect(layoutEnumerator.text).toEqual("¶");
```

### See Also

* module [Aspose.Words.Layout](../)

