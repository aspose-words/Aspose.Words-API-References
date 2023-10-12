---
title: Cell.FirstParagraph
second_title: Referencia de API de Aspose.Words para .NET
description: Cell propiedad. Obtiene el primer párrafo entre los hijos inmediatos.
type: docs
weight: 30
url: /es/net/aspose.words.tables/cell/firstparagraph/
---
## Cell.FirstParagraph property

Obtiene el primer párrafo entre los hijos inmediatos.

```csharp
public Paragraph FirstParagraph { get; }
```

### Ejemplos

Muestra cómo crear una tabla anidada utilizando un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Construye la tabla exterior.
Cell cell = builder.InsertCell();
builder.Writeln("Outer Table Cell 1");
builder.InsertCell();
builder.Writeln("Outer Table Cell 2");
builder.EndTable();

// Pasar a la primera celda de la tabla exterior y crear otra tabla dentro de la celda.
builder.MoveTo(cell.FirstParagraph);
builder.InsertCell();
builder.Writeln("Inner Table Cell 1");
builder.InsertCell();
builder.Writeln("Inner Table Cell 2");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertNestedTable.docx");
```

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../cell/)
* asamblea [Aspose.Words](../../../)


