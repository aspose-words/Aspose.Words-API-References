---
title: TextColumn class
linktitle: TextColumn class
articleTitle: TextColumn class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.TextColumn class. Represents a single text column"
type: docs
weight: 1370
url: /nodejs-net/aspose.words/textcolumn/
---

## TextColumn class

Represents a single text column. [TextColumn](./) is a member of the [TextColumnCollection](../textcolumncollection/) collection.
The [TextColumn](./) collection includes all the columns in a section of a document.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/nodejs-net/working-with-sections/) documentation article.




### Remarks

[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want
the columns in the document to be of equal width, set TextColumns.[TextColumnCollection.evenlySpaced](../textcolumncollection/evenlySpaced/) to ``true``.

When a new [TextColumn](./) is created it has its width and spacing set to zero.




### Properties

| Name | Description |
| --- | --- |
| [spaceAfter](./spaceAfter/) | Gets or sets the space between this column and the next column in points. Not required for the last column. |
| [width](./width/) | Gets or sets the width of the text column in points. |

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

* module [Aspose.Words](../)
* class [TextColumnCollection](../textcolumncollection/)
* class [PageSetup](../pagesetup/)
* class [Section](../section/)

