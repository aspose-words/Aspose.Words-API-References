---
title: TextWrapping enumeration
linktitle: TextWrapping enumeration
articleTitle: TextWrapping enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Tables.TextWrapping enumeration. Specifies how text is wrapped around the table."
type: docs
weight: 150
url: /nodejs-net/aspose.words.tables/textwrapping/
---

## TextWrapping enumeration

Specifies how text is wrapped around the table.


### Members

| Name | Description |
| --- | --- |
| None | Text and table is displayed in the order of their appearance in the document. |
| Around | Text is wrapped around the table occupying available side space. |
| Default | Default value. |

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

* module [Aspose.Words.Tables](../)

