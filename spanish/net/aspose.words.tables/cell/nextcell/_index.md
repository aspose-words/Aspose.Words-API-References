---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words para .NET
description: Descubra la propiedad NextCell para acceder fácilmente al próximo nodo Cell, mejorando la gestión de sus datos y agilizando su flujo de trabajo.
type: docs
weight: 70
url: /es/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Obtiene el siguiente[`Cell`](../) nodo.

```csharp
public Cell NextCell { get; }
```

## Observaciones

El método se puede utilizar cuando se necesita tener acceso escrito a las celdas de una[`Row`](../../row/) . Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Si el nodo se encuentra en una fila en lugar de en una celda, se recorre automáticamente para obtener una celda contenida dentro.

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

* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
