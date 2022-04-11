---
title: "Cell"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 5850
url: /net/aspose.words.tables/cell/
---
## Cell class

Represents a table cell.

```csharp
public class Cell : CompositeNode
```

## Public Members

| Name | Description |
| --- | --- |
| [Cell](cell)(…) | Initializes a new instance of the Cell class. |
| [CellFormat](cellformat) { get; } | Provides access to the formatting properties of the cell. |
| [FirstParagraph](firstparagraph) { get; } | Gets the first paragraph among the immediate children. |
| [IsFirstCell](isfirstcell) { get; } | True if this is the first cell inside a row; false otherwise. |
| [IsLastCell](islastcell) { get; } | True if this is the last cell inside a row; false otherwise. |
| [LastParagraph](lastparagraph) { get; } | Gets the last paragraph among the immediate children. |
| override [NodeType](nodetype) { get; } | Returns NodeType.Cell. |
| [Paragraphs](paragraphs) { get; } | Gets a collection of paragraphs that are immediate children of the cell. |
| [ParentRow](parentrow) { get; } | Returns the parent row of the cell. |
| [Tables](tables) { get; } | Gets a collection of tables that are immediate children of the cell. |
| override [Accept](accept)(…) | Accepts a visitor. |
| [EnsureMinimum](ensureminimum)() | If the last child is not a paragraph, creates and appends one empty paragraph. |

### Remarks

Cell can only be a child of a Row.Cell can contain block-level nodes Paragraph and Table.A minimal valid cell needs to have at least one Paragraph.

### Examples

Shows how to create a table.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tables contain rows, which contain cells, which may have paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row, cell, and paragraph.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Add text to the first call in the first row of the table.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Shows how to iterate through all tables in the document and print the contents of each cell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // We can use the "ToArray" method on a row collection to clone it into an array.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // We can use the "ToArray" method on a cell collection to clone it into an array.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

Shows how to build a nested table without using a document builder.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Create the outer table with three rows and four columns, and then add it to the document.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Create another table with two rows and two columns and then insert it into the first table's first cell.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

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

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
