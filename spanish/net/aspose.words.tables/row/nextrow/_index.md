---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words para .NET
description: Descubra la propiedad NextRow para acceder sin esfuerzo al siguiente nodo Fila, mejorando su experiencia de navegación y gestión de datos.
type: docs
weight: 70
url: /es/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Obtiene el siguiente[`Row`](../) nodo.

```csharp
public Row NextRow { get; }
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
