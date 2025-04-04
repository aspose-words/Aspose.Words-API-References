---
title: DocumentBuilder.moveToCell method
linktitle: moveToCell method
articleTitle: moveToCell method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.moveToCell method. Moves the cursor to a table cell in the current section."
type: docs
weight: 540
url: /nodejs-net/aspose.words/documentbuilder/moveToCell/
---

## moveToCell(tableIndex, rowIndex, columnIndex, characterIndex) {#number_number_number_number}

Moves the cursor to a table cell in the current section.


```js
moveToCell(tableIndex: number, rowIndex: number, columnIndex: number, characterIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | number | The index of the table to move to. |
| rowIndex | number | The index of the row in the table. |
| columnIndex | number | The index of the column in the table. |
| characterIndex | number | The index of the character inside the cell. A negative value allows you to specify a position from the end of the cell. Use -1 to move to the end of the cell. |

### Remarks

The navigation is performed inside the current story of the current section.

For the index parameters, when index is greater than or equal to 0, it specifies an index from
the beginning with 0 being the first element. When index is less than 0, it specified an index from
the end with -1 being the last element.




### Examples

Shows how to move a document builder's cursor to a cell in a table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create an empty 2x2 table.
builder.startTable();
builder.insertCell();
builder.insertCell();
builder.endRow();
builder.insertCell();
builder.insertCell();
builder.endTable();

// Because we have ended the table with the EndTable method,
// the document builder's cursor is currently outside the table.
// This cursor has the same function as Microsoft Word's blinking text cursor.
// It can also be moved to a different location in the document using the builder's MoveTo methods.
// We can move the cursor back inside the table to a specific cell.
builder.moveToCell(0, 1, 1, 0);
builder.write("Column 2, cell 2.");

doc.save(base.artifactsDir + "DocumentBuilder.moveToCell.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

