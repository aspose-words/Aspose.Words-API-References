---
title: Cell.Cell
second_title: Aspose.Words for .NET API Reference
description: Cell constructor. Initializes a new instance of the Cell class in C#.
type: docs
weight: 10
url: /net/aspose.words.tables/cell/cell/
---
## Cell constructor

Initializes a new instance of the [`Cell`](../) class.

```csharp
public Cell(DocumentBase doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |

## Remarks

When [`Cell`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../../aspose.words/node/parentnode/) is `null`.

To append [`Cell`](../) to the document use [`InsertAfter`](../../../aspose.words/compositenode/insertafter/) or [`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) on the row where you want the cell inserted.

## Examples

Shows how to build a nested table without using a document builder.

```csharp
{
    Document doc = new Document();

    // Create the outer table with three rows and four columns, and then add it to the document.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Create another table with two rows and two columns and then insert it into the first table's first cell.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");

/// <summary>
/// Creates a new table in the document with the given dimensions and text in each cell.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
    // The table must have at least one row before we can use these properties.
    // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
    // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### See Also

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Cell](../)
* namespace [Aspose.Words.Tables](../../cell/)
* assembly [Aspose.Words](../../../)
