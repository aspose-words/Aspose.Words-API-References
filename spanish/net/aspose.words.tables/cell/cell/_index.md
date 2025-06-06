---
title: Cell
linktitle: Cell
articleTitle: Cell
second_title: Aspose.Words para .NET
description: Descubre el constructor Cell para crear fácilmente nuevas instancias de la clase Cell. ¡Optimiza tu proceso de codificación y mejora tu eficiencia de desarrollo!
type: docs
weight: 10
url: /es/net/aspose.words.tables/cell/cell/
---
## Cell constructor

Inicializa una nueva instancia del[`Cell`](../) clase.

```csharp
public Cell(DocumentBase doc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | DocumentBase | El documento del propietario. |

## Observaciones

Cuando[`Cell`](../) se crea, pertenece al documento especificado, pero aún no es parte del documento y[`ParentNode`](../../../aspose.words/node/parentnode/) es`nulo`.

Para anexar[`Cell`](../) al uso del documento[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) o[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) en la fila donde desea insertar la celda.

## Ejemplos

Muestra cómo construir una tabla anidada sin utilizar un generador de documentos.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Cree la tabla externa con tres filas y cuatro columnas y luego agréguela al documento.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Cree otra tabla con dos filas y dos columnas y luego insértela en la primera celda de la primera tabla.
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

    // Puede utilizar las propiedades "Título" y "Descripción" para agregar un título y una descripción respectivamente a su tabla.
    //La tabla debe tener al menos una fila antes de que podamos usar estas propiedades.
    // Estas propiedades son significativas para los documentos .docx compatibles con ISO/IEC 29500 (consulte la clase OoxmlCompliance).
    // Si guardamos el documento en formatos anteriores a ISO/IEC 29500, Microsoft Word ignora estas propiedades.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ver también

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
