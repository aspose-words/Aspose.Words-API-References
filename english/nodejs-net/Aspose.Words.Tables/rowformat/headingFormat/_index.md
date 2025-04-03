---
title: RowFormat.headingFormat property
linktitle: headingFormat property
articleTitle: headingFormat property
second_title: Aspose.Words for NodeJs
description: "RowFormat.headingFormat property. True if the row is repeated as a table heading on every page when the table spans more than one page."
type: docs
weight: 30
url: /nodejs-net/aspose.words.tables/rowformat/headingFormat/
---

## RowFormat.headingFormat property

True if the row is repeated as a table heading on every page when the table spans more than one page.


```js
get headingFormat(): boolean
```

### Examples

Shows how to build a table with rows that repeat on every page.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();

// Any rows inserted while the "HeadingFormat" flag is set to "true"
// will show up at the top of the table on every page that it spans.
builder.rowFormat.headingFormat = true;
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
builder.cellFormat.width = 100;
builder.insertCell();
builder.write("Heading row 1");
builder.endRow();
builder.insertCell();
builder.write("Heading row 2");
builder.endRow();

builder.cellFormat.width = 50;
builder.paragraphFormat.clearFormatting();
builder.rowFormat.headingFormat = false;

// Add enough rows for the table to span two pages.
for (let i = 0; i < 50; i++)
{
  builder.insertCell();
  builder.write(`Row ${table.rows.count}, column 1.`);
  builder.insertCell();
  builder.write(`Row ${table.rows.count}, column 2.`);
  builder.endRow();
}

doc.save(base.artifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [RowFormat](../)

