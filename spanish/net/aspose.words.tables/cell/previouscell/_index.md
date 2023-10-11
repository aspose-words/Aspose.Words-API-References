---
title: Cell.PreviousCell
second_title: Referencia de API de Aspose.Words para .NET
description: Cell propiedad. Obtiene el anteriorCell nodo.
type: docs
weight: 110
url: /es/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

Obtiene el anterior[`Cell`](../) nodo.

```csharp
public Cell PreviousCell { get; }
```

### Observaciones

El método se puede utilizar cuando necesita tener acceso escrito a las celdas de un[`Row`](../../row/) . Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Si un nodo se encuentra en una fila en lugar de en una celda, se recorre automáticamente para obtener una celda contenida dentro.

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

* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../cell/)
* asamblea [Aspose.Words](../../../)


