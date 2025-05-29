---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words para .NET
description: Acceda a la propiedad PreviousRow para recuperar fácilmente el nodo Row anterior, mejorando su navegación de datos y agilizando su flujo de trabajo de codificación.
type: docs
weight: 100
url: /es/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

Obtiene el anterior[`Row`](../) nodo.

```csharp
public Row PreviousRow { get; }
```

## Observaciones

El método se puede usar cuando se necesita acceso tipificado a las filas de la tabla. Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) El nodo se encuentra en una tabla en lugar de en una fila, se recorre automáticamente para obtener una fila contenida dentro.

## Ejemplos

Muestra cómo enumerar todas las celdas de la tabla.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Enumerar todas las celdas de la tabla.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Ver también

* class [Row](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
