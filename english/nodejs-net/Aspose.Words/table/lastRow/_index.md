---
title: Table.lastRow property
linktitle: lastRow property
articleTitle: lastRow property
second_title: Aspose.Words for NodeJs
description: "Table.lastRow property. Returns the last [Row](../../../aspose.words.tables/row/) node in the table."
type: docs
weight: 180
url: /nodejs-net/aspose.words/table/lastRow/
---

## Table.lastRow property

Returns the last [Row](../../../aspose.words.tables/row/) node in the table.



```js
get lastRow(): Aspose.Words.Tables.Row
```

### Examples

Shows how to remove the first and last rows of all tables in a document.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");

let tables = doc.firstSection.body.tables.toArray();

expect(tables[0].rows.count).toEqual(5);
expect(tables[1].rows.count).toEqual(4);

for (var table of tables)
{
  table.firstRow?.remove();
  table.lastRow?.remove();
}

expect(tables[0].rows.count).toEqual(3);
expect(tables[1].rows.count).toEqual(2);
```

### See Also

* module [Aspose.Words](../../)
* class [Table](../)

