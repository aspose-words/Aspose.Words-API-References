---
title: Bookmark.FirstColumn
linktitle: FirstColumn
articleTitle: FirstColumn
second_title: Aspose.Words para .NET
description: Bookmark FirstColumn propiedad. Obtiene el índice de base cero de la primera columna del rango de columnas de la tabla asociado con el marcador en C#.
type: docs
weight: 30
url: /es/net/aspose.words/bookmark/firstcolumn/
---
## Bookmark.FirstColumn property

Obtiene el índice de base cero de la primera columna del rango de columnas de la tabla asociado con el marcador.

```csharp
public int FirstColumn { get; }
```

## Observaciones

Devoluciones**-1** si este marcador no es un marcador de columna de tabla.

## Ejemplos

Muestra cómo obtener información sobre los marcadores de columnas de la tabla.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Si un marcador encierra columnas de una tabla, es un marcador de columna de tabla y su indicador IsColumn está establecido en verdadero.
    Console.WriteLine($"Bookmark: {bookmark.Name}{(bookmark.IsColumn ? " (Column)" : "")}");
    if (bookmark.IsColumn)
    {
        if (bookmark.BookmarkStart.GetAncestor(NodeType.Row) is Row row &&
            bookmark.FirstColumn < row.Cells.Count)
        {
            // Imprime el contenido de la primera y última columna encerradas por el marcador.
            Console.WriteLine(row.Cells[bookmark.FirstColumn].GetText().TrimEnd(ControlChar.CellChar));
            Console.WriteLine(row.Cells[bookmark.LastColumn].GetText().TrimEnd(ControlChar.CellChar));
        }
    }
}
```

### Ver también

* class [Bookmark](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
