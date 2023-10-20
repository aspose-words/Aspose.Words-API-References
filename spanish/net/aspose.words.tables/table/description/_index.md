---
title: Table.Description
linktitle: Description
articleTitle: Description
second_title: Aspose.Words para .NET
description: Table Description propiedad. Obtiene o establece la descripción de esta tabla. Proporciona una representación de texto alternativa de la información contenida en la tabla en C#.
type: docs
weight: 110
url: /es/net/aspose.words.tables/table/description/
---
## Table.Description property

Obtiene o establece la descripción de esta tabla. Proporciona una representación de texto alternativa de la información contenida en la tabla.

```csharp
public string Description { get; set; }
```

## Observaciones

El valor predeterminado es una cadena vacía.

Esta propiedad es significativa para documentos DOCX compatibles con ISO/IEC 29500 ([`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). Cuando se guarda en formatos anteriores a ISO/IEC 29500, la propiedad se ignora.

## Ejemplos

Muestra cómo crear una tabla anidada sin utilizar un generador de documentos.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Cree la tabla exterior con tres filas y cuatro columnas y luego agréguela al documento.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Crea otra tabla con dos filas y dos columnas y luego insértala en la primera celda de la primera tabla.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Crea una nueva tabla en el documento con las dimensiones y el texto dados en cada celda.
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

    // Puedes usar las propiedades "Título" y "Descripción" para agregar un título y una descripción respectivamente a tu tabla.
    // La tabla debe tener al menos una fila antes de que podamos usar estas propiedades.
    // Estas propiedades son significativas para documentos .docx compatibles con ISO/IEC 29500 (consulte la clase OoxmlCompliance).
    // Si guardamos el documento en formatos anteriores a ISO/IEC 29500, Microsoft Word ignora estas propiedades.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
