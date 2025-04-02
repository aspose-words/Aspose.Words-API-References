---
title: TextColumn.spaceAfter property
linktitle: spaceAfter property
articleTitle: spaceAfter property
second_title: Aspose.Words for NodeJs
description: "TextColumn.spaceAfter property. Gets or sets the space between this column and the next column in points"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/textcolumn/spaceAfter/
---

## TextColumn.spaceAfter property

Gets or sets the space between this column and the next column in points. Not required for the last column.


```js
get spaceAfter(): number
```

### Examples

Shows how to create unevenly spaced columns.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let pageSetup = builder.pageSetup;

let columns = pageSetup.textColumns;
columns.evenlySpaced = false;
columns.setCount(2);

// Determine the amount of room that we have available for arranging columns.
var contentWidth = pageSetup.pageWidth - pageSetup.leftMargin - pageSetup.rightMargin;

expect(contentWidth).toBeCloseTo(468, 1);

// Set the first column to be narrow.
let column = columns.at(0);
column.width = 100;
column.spaceAfter = 20;

// Set the second column to take the rest of the space available within the margins of the page.
column = columns.at(1);
column.width = contentWidth - column.width - column.spaceAfter;

builder.writeln("Narrow column 1.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.writeln("Wide column 2.");

doc.save(base.artifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TextColumn](../)

