---
title: Bookmark.LastColumn
linktitle: LastColumn
articleTitle: LastColumn
second_title: Aspose.Words para .NET
description: Descubra la propiedad LastColumn, acceda fácilmente al índice basado en cero de la última columna en el rango de marcadores de su tabla para una gestión de datos eficiente.
type: docs
weight: 50
url: /es/net/aspose.words/bookmark/lastcolumn/
---
## Bookmark.LastColumn property

Obtiene el índice basado en cero de la última columna del rango de columnas de la tabla asociada con el marcador.

```csharp
public int LastColumn { get; }
```

## Observaciones

Devuelve**-1** Si este marcador no es un marcador de columna de tabla.

## Ejemplos

Muestra cómo obtener información sobre los marcadores de columnas de la tabla.

```csharp
Document doc = new Document(MyDir + "Table column bookmarks.doc");

foreach (Bookmark bookmark in doc.Range.Bookmarks)
{
    // Si un marcador encierra columnas de una tabla, es un marcador de columna de tabla y su indicador IsColumn se establece en verdadero.
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
