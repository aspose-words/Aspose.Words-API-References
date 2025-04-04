---
title: RowFormat.allowBreakAcrossPages property
linktitle: allowBreakAcrossPages property
articleTitle: allowBreakAcrossPages property
second_title: Aspose.Words for Node.js
description: "RowFormat.allowBreakAcrossPages property. True if the text in a table row is allowed to split across a page break."
type: docs
weight: 10
url: /nodejs-net/aspose.words.tables/rowformat/allowBreakAcrossPages/
---

## RowFormat.allowBreakAcrossPages property

True if the text in a table row is allowed to split across a page break.


```js
get allowBreakAcrossPages(): boolean
```

### Examples

Shows how to disable rows breaking across pages for every row in a table.

```js
let doc = new aw.Document(base.myDir + "Table spanning two pages.docx");
let table = doc.firstSection.body.tables.at(0);

// Set the "AllowBreakAcrossPages" property to "false" to keep the row
// in one piece if a table spans two pages, which break up along that row.
// If the row is too big to fit in one page, Microsoft Word will push it down to the next page.
// Set the "AllowBreakAcrossPages" property to "true" to allow the row to break up across two pages.
for (let row of table.rows.toArray())
  row.rowFormat.allowBreakAcrossPages = allowBreakAcrossPages;

doc.save(base.artifactsDir + "Table.allowBreakAcrossPages.docx");
```

### See Also

* module [Aspose.Words.Tables](../../)
* class [RowFormat](../)

