---
title: Table.textWrapping property
linktitle: textWrapping property
articleTitle: textWrapping property
second_title: Aspose.Words for NodeJs
description: "Table.textWrapping property. Gets or sets [Table.textWrapping](./) for table."
type: docs
weight: 310
url: /nodejs-net/aspose.words/table/textWrapping/
---

## Table.textWrapping property

Gets or sets [Table.textWrapping](./) for table.



```js
get textWrapping(): Aspose.Words.Tables.TextWrapping
```

### Examples

Shows how to work with table text wrapping.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Cell 1");
builder.insertCell();
builder.write("Cell 2");
builder.endTable();
table.preferredWidth = aw.Tables.PreferredWidth.fromPoints(300);

builder.font.size = 16;
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
// and push it down into the paragraph below by setting the position.
table.textWrapping = aw.Tables.TextWrapping.Around;
table.absoluteHorizontalDistance = 100;
table.absoluteVerticalDistance = 20;

doc.save(base.artifactsDir + "Table.wrapText.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

