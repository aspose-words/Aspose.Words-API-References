---
title: DocumentBuilder.deleteRow method
linktitle: deleteRow method
articleTitle: deleteRow method
second_title: Aspose.Words for NodeJs
description: "DocumentBuilder.deleteRow method. Deletes a row from a table."
type: docs
weight: 200
url: /nodejs-net/aspose.words/documentbuilder/deleteRow/
---

## deleteRow(tableIndex, rowIndex) {#number_number}

Deletes a row from a table.


```js
deleteRow(tableIndex: numberrowIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | number | The index of the table. |
| rowIndex | number | The index of the row in the table. |

### Remarks

If the cursor is inside the row that is being deleted, the cursor is moved
out to the next row or to the next paragraph after the table.

If you delete a row from a table that contains only one row, the whole
table is deleted.

For the index parameters, when index is greater than or equal to 0, it specifies an index from
the beginning with 0 being the first element. When index is less than 0, it specified an index from
the end with -1 being the last element.




### Returns

The row node that was just removed.


### Examples

Shows how to delete a row from a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Row 1, cell 1.");
builder.insertCell();
builder.write("Row 1, cell 2.");
builder.endRow();
builder.insertCell();
builder.write("Row 2, cell 1.");
builder.insertCell();
builder.write("Row 2, cell 2.");
builder.endTable();

expect(table.rows.count).toEqual(2);

// Delete the first row of the first table in the document.
builder.deleteRow(0, 0);

expect(table.rows.count).toEqual(1);
expect(table.getText().trim()).toEqual("Row 2, cell 1.\u0007Row 2, cell 2.\u0007\u0007");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

