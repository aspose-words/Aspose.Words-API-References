---
title: "Table"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 5950
url: /net/aspose.words.tables/table/
---
## Table class

Represents a table in a Word document.

```csharp
public class Table : CompositeNode
```

## Public Members

| Name | Description |
| --- | --- |
| [Table](table)(…) | Initializes a new instance of the Table class. |
| [AbsoluteHorizontalDistance](absolutehorizontaldistance) { get; set; } | Gets or sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0. |
| [AbsoluteVerticalDistance](absoluteverticaldistance) { get; set; } | Gets or sets absolute vertical floating table position specified by the table properties, in points. Default value is 0. |
| [Alignment](alignment) { get; set; } | Specifies how an inline table is aligned in the document. |
| [AllowAutoFit](allowautofit) { get; set; } | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [AllowCellSpacing](allowcellspacing) { get; set; } | Gets or sets the "Allow spacing between cells" option. |
| [AllowOverlap](allowoverlap) { get; } | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is `true`. |
| [Bidi](bidi) { get; set; } | Gets or sets whether this is a right-to-left table. |
| [BottomPadding](bottompadding) { get; set; } | Gets or sets the amount of space (in points) to add below the contents of cells. |
| [CellSpacing](cellspacing) { get; set; } | Gets or sets the amount of space (in points) between the cells. |
| [Description](description) { get; set; } | Gets or sets description of this table. It provides an alternative text representation of the information contained in the table. |
| [DistanceBottom](distancebottom) { get; } | Gets distance between table bottom and the surrounding text, in points. |
| [DistanceLeft](distanceleft) { get; } | Gets distance between table left and the surrounding text, in points. |
| [DistanceRight](distanceright) { get; } | Gets distance between table right and the surrounding text, in points. |
| [DistanceTop](distancetop) { get; } | Gets distance between table top and the surrounding text, in points. |
| [FirstRow](firstrow) { get; } | Returns the first Row node in the table. |
| [HorizontalAnchor](horizontalanchor) { get; set; } | Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is Column. |
| [LastRow](lastrow) { get; } | Returns the last Row node in the table. |
| [LeftIndent](leftindent) { get; set; } | Gets or sets the value that represents the left indent of the table. |
| [LeftPadding](leftpadding) { get; set; } | Gets or sets the amount of space (in points) to add to the left of the contents of cells. |
| override [NodeType](nodetype) { get; } | Returns NodeType.Table. |
| [PreferredWidth](preferredwidth) { get; set; } | Gets or sets the table preferred width. |
| [RelativeHorizontalAlignment](relativehorizontalalignment) { get; set; } | Gets or sets floating table relative horizontal alignment. |
| [RelativeVerticalAlignment](relativeverticalalignment) { get; set; } | Gets or sets floating table relative vertical alignment. |
| [RightPadding](rightpadding) { get; set; } | Gets or sets the amount of space (in points) to add to the right of the contents of cells. |
| [Rows](rows) { get; } | Provides typed access to the rows of the table. |
| [Style](style) { get; set; } | Gets or sets the table style applied to this table. |
| [StyleIdentifier](styleidentifier) { get; set; } | Gets or sets the locale independent style identifier of the table style applied to this table. |
| [StyleName](stylename) { get; set; } | Gets or sets the name of the table style applied to this table. |
| [StyleOptions](styleoptions) { get; set; } | Gets or sets bit flags that specify how a table style is applied to this table. |
| [TextWrapping](textwrapping) { get; set; } | Gets or sets [`TextWrapping`](./textwrapping) for table. |
| [Title](title) { get; set; } | Gets or sets title of this table. It provides an alternative text representation of the information contained in the table. |
| [TopPadding](toppadding) { get; set; } | Gets or sets the amount of space (in points) to add above the contents of cells. |
| [VerticalAnchor](verticalanchor) { get; set; } | Gets the base object from which the vertical positioning of floating table should be calculated. Default value is Margin. |
| override [Accept](accept)(…) | Accepts a visitor. |
| [AutoFit](autofit)(…) | Resizes the table and cells according to the specified auto fit behavior. |
| [ClearBorders](clearborders)() | Removes all table and cell borders on this table. |
| [ClearShading](clearshading)() | Removes all shading on the table. |
| [ConvertToHorizontallyMergedCells](converttohorizontallymergedcells)() | Converts cells horizontally merged by width to cells merged by [`HorizontalMerge`](../cellformat/horizontalmerge). |
| [EnsureMinimum](ensureminimum)() | If the table has no rows, creates and appends one Row. |
| [SetBorder](setborder)(…) | Sets the specified table border to the specified line style, width and color. |
| [SetBorders](setborders)(…) | Sets all table borders to the specified line style, width and color. |
| [SetShading](setshading)(…) | Sets shading to the specified values on whole table. |

### Remarks

Table is a block-level node and can be a child of classes derived from Story or InlineStory.Table can contain one or more Row nodes.A minimal valid table needs to have at least one Row.

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

Shows how to build a formatted 2x2 table.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
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
