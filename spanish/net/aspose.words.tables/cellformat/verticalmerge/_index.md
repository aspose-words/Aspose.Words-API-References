---
title: CellFormat.VerticalMerge
linktitle: VerticalMerge
articleTitle: VerticalMerge
second_title: Aspose.Words para .NET
description: CellFormat VerticalMerge propiedad. Especifica cómo se fusiona la celda con otras celdas verticalmente en C#.
type: docs
weight: 120
url: /es/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

Especifica cómo se fusiona la celda con otras celdas verticalmente.

```csharp
public CellMerge VerticalMerge { get; set; }
```

## Observaciones

Las celdas sólo se pueden fusionar verticalmente si sus límites izquierdo y derecho son idénticos.

Cuando las celdas se fusionan verticalmente, las áreas de visualización de las celdas fusionadas se consolidan. El área consolidada se utiliza para mostrar el contenido de la primera celda fusionada verticalmente y todas las demás celdas fusionadas verticalmente deben estar vacías.

## Ejemplos

Imprime el tipo de combinación horizontal y vertical de una celda.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows.OfType<Row>())
        foreach (Cell cell in row.Cells.OfType<Cell>())
            Console.WriteLine(PrintCellMergeType(cell));
}

public string PrintCellMergeType(Cell cell)
{
    bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
    bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
    string cellLocation =
        $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";

    if (isHorizontallyMerged && isVerticallyMerged)
        return $"The cell at {cellLocation} is both horizontally and vertically merged";
    if (isHorizontallyMerged)
        return $"The cell at {cellLocation} is horizontally merged.";

    return isVerticallyMerged ? $"The cell at {cellLocation} is vertically merged" : $"The cell at {cellLocation} is not merged";
}
```

Muestra cómo fusionar celdas de tablas verticalmente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una celda en la primera columna de la primera fila.
// Esta celda será la primera de un rango de celdas fusionadas verticalmente.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Inserta una celda en la segunda columna de la primera fila, luego finaliza la fila.
// Además, configure el generador para deshabilitar la combinación vertical en las celdas creadas.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Inserta una celda en la primera columna de la segunda fila.
// En lugar de agregar contenido de texto, fusionaremos esta celda con la primera celda que agregamos directamente arriba.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Inserta otra celda independiente en la segunda columna de la segunda fila.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Ver también

* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
