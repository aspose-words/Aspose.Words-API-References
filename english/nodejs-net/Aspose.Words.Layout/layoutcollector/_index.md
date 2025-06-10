---
title: LayoutCollector class
linktitle: LayoutCollector class
articleTitle: LayoutCollector class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Layout.LayoutCollector class. This class allows to compute page numbers of document nodes."
type: docs
weight: 40
url: /nodejs-net/aspose.words.layout/layoutcollector/
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

### See Also

* module [Aspose.Words.Layout](../)

