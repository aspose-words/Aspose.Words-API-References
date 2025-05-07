---
title: TextColumnCollection.lineBetween property
linktitle: lineBetween property
articleTitle: lineBetween property
second_title: Aspose.Words for Node.js
description: "TextColumnCollection.lineBetween property. When ``true``, adds a vertical line between columns."
type: docs
weight: 30
url: /nodejs-net/aspose.words/textcolumncollection/lineBetween/
---

## TextColumnCollection.lineBetween property

When ``true``, adds a vertical line between columns.



```js
get lineBetween(): boolean
```

### Examples

Shows how to separate columns with a vertical line.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Configure the current section's PageSetup object to divide the text into several columns.
// Set the "LineBetween" property to "true" to put a dividing line between columns.
// Set the "LineBetween" property to "false" to leave the space between columns blank.
let columns = builder.pageSetup.textColumns;
columns.lineBetween = lineBetween;
columns.setCount(3);

builder.writeln("Column 1.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.writeln("Column 2.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.writeln("Column 3.");

doc.save(base.artifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [TextColumnCollection](../)

