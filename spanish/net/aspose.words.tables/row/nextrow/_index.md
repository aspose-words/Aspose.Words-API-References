---
title: Row.NextRow
second_title: Referencia de API de Aspose.Words para .NET
description: Row propiedad. Obtiene el siguienteRow nodo.
type: docs
weight: 70
url: /es/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

Obtiene el siguiente[`Row`](../) nodo.

```csharp
public Row NextRow { get; }
```

### Observaciones

El método se puede utilizar cuando necesita tener acceso escrito a las filas de la tabla. Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)El nodo se encuentra en una tabla en lugar de en una fila, se recorre automáticamente para obtener una fila contenida dentro.

### Ejemplos

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
* espacio de nombres [Aspose.Words.Tables](../../row/)
* asamblea [Aspose.Words](../../../)


