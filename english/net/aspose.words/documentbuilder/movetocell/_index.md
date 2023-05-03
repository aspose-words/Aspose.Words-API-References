---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder MoveToCell method. Moves the cursor to a table cell in the current section in C#.
type: docs
weight: 500
url: /net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Moves the cursor to a table cell in the current section.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | Int32 | The index of the table to move to. |
| rowIndex | Int32 | The index of the row in the table. |
| columnIndex | Int32 | The index of the column in the table. |
| characterIndex | Int32 | The index of the character inside the cell. A negative value allows you to specify a position from the end of the cell. Use -1 to move to the end of the cell. |

## Remarks

The navigation is performed inside the current story of the current section.

For the index parameters, when index is greater than or equal to 0, it specifies an index from the beginning with 0 being the first element. When index is less than 0, it specified an index from the end with -1 being the last element.

## Examples

Shows how to move a document builder's cursor to a cell in a table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create an empty 2x2 table.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Because we have ended the table with the EndTable method,
// the document builder's cursor is currently outside the table.
// This cursor has the same function as Microsoft Word's blinking text cursor.
// It can also be moved to a different location in the document using the builder's MoveTo methods.
// We can move the cursor back inside the table to a specific cell.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
