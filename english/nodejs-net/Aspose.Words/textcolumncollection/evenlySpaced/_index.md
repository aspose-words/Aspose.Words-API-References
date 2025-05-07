---
title: TextColumnCollection.evenlySpaced property
linktitle: evenlySpaced property
articleTitle: evenlySpaced property
second_title: Aspose.Words for Node.js
description: "TextColumnCollection.evenlySpaced property. True if text columns are of equal width and evenly spaced."
type: docs
weight: 20
url: /nodejs-net/aspose.words/textcolumncollection/evenlySpaced/
---

## TextColumnCollection.evenlySpaced property

True if text columns are of equal width and evenly spaced.


```js
get evenlySpaced(): boolean
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
* class [TextColumnCollection](../)

