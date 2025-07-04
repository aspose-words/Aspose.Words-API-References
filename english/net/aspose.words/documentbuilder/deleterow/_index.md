---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words for .NET
description: Effortlessly remove rows from tables with the DocumentBuilder DeleteRow method. Streamline your document editing and enhance your workflow!
type: docs
weight: 200
url: /net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

Deletes a row from a table.

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | Int32 | The index of the table. |
| rowIndex | Int32 | The index of the row in the table. |

### Return Value

The row node that was just removed.

## Remarks

If the cursor is inside the row that is being deleted, the cursor is moved out to the next row or to the next paragraph after the table.

If you delete a row from a table that contains only one row, the whole table is deleted.

For the index parameters, when index is greater than or equal to 0, it specifies an index from the beginning with 0 being the first element. When index is less than 0, it specified an index from the end with -1 being the last element.

## Examples

Shows how to delete a row from a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.That(table.Rows.Count, Is.EqualTo(2));

// Delete the first row of the first table in the document.
builder.DeleteRow(0, 0);

Assert.That(table.Rows.Count, Is.EqualTo(1));
Assert.That(table.GetText().Trim(), Is.EqualTo("Row 2, cell 1.\aRow 2, cell 2.\a\a"));
```

### See Also

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
