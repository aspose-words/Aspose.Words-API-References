---
title: LayoutCollector.getEndPageIndex method
linktitle: getEndPageIndex method
articleTitle: getEndPageIndex method
second_title: Aspose.Words for Node.js
description: "LayoutCollector.getEndPageIndex method. Gets 1-based index of the page where node ends"
type: docs
weight: 40
url: /nodejs-net/aspose.words.layout/layoutcollector/getEndPageIndex/
---

## getEndPageIndex(node) {#node}

Gets 1-based index of the page where node ends. Returns 0 if node cannot be mapped to a page.


```js
getEndPageIndex(node: Aspose.Words.Node)
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../../aspose.words/node/) |  |

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

* module [Aspose.Words.Layout](../../)
* class [LayoutCollector](../)

