---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Tables.CellMerge para una combinación eficiente de celdas de tabla. Mejore el diseño de sus documentos con una integración y flexibilidad perfectas.
type: docs
weight: 7120
url: /es/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Especifica cómo se fusiona una celda de una tabla con otras celdas.

```csharp
public enum CellMerge
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | La celda no está fusionada. |
| First | `1` | La celda es la primera celda de un rango de celdas fusionadas. |
| Previous | `2` | La celda se fusiona con la celda anterior horizontal o verticalmente. |

## Ejemplos

Muestra cómo fusionar celdas de una tabla horizontalmente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una celda en la primera columna de la primera fila.
// Esta celda será la primera de un rango de celdas fusionadas horizontalmente.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Insertar una celda en la segunda columna de la primera fila. En lugar de añadir texto,
// Fusionaremos esta celda con la primera celda que agregamos directamente a la izquierda.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Inserta dos celdas más no fusionadas en la segunda fila.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Imprime el tipo de combinación horizontal y vertical de una celda.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows)
        foreach (Cell cell in row.Cells)
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

Muestra cómo fusionar celdas de una tabla verticalmente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una celda en la primera columna de la primera fila.
// Esta celda será la primera de un rango de celdas fusionadas verticalmente.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Inserta una celda en la segunda columna de la primera fila y luego finaliza la fila.
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

* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)
