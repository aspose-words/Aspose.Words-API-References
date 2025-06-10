---
title: TextColumnCollection class
linktitle: TextColumnCollection class
articleTitle: TextColumnCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TextColumnCollection class. A collection of [TextColumn](../textcolumn/) objects that represent all the columns of text in a section of a document"
type: docs
weight: 1350
url: /nodejs-net/aspose.words/textcolumncollection/
---

## TextColumnCollection class

A collection of [TextColumn](../textcolumn/) objects that represent all the columns of text in a section of a document.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/nodejs-net/working-with-sections/) documentation article.




### Remarks

Use [TextColumnCollection.setCount()](./setCount/#number) to set the number of text columns.

To make all columns equal width and spaced evenly, set [TextColumnCollection.evenlySpaced](./evenlySpaced/) to ``true``
and specify the amount of space between the columns in [TextColumnCollection.spacing](./spacing/). MS Word will
automatically calculate column widths.

If you have [TextColumnCollection.evenlySpaced](./evenlySpaced/) set to ``false``, you need to specify width and spacing for each
column individually. Use the indexer to access individual [TextColumn](../textcolumn/) objects.

When using custom column widths, make sure the sum of all column widths and spacings between them
equals page width minus left and right page margins.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of columns in the section of a document. |
| [evenlySpaced](./evenlySpaced/) | True if text columns are of equal width and evenly spaced. |
| [lineBetween](./lineBetween/) | When ``true``, adds a vertical line between columns. |
| [spacing](./spacing/) | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
| [this[]](./this[]/) |  |
| [width](./width/) | When columns are evenly spaced, gets the width of the columns. |

### Methods

| Name | Description |
| --- | --- |
|[ setCount(newCount)](./setCount/#number) | Arranges text into the specified number of text columns. |

### Examples

Shows how to create multiple evenly spaced columns in a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let columns = builder.pageSetup.textColumns;
columns.spacing = 100;
columns.setCount(2);

builder.writeln("Column 1.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.writeln("Column 2.");

doc.save(base.artifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### See Also

* module [Aspose.Words](../)
* class [PageSetup](../pagesetup/)
* class [Section](../section/)

