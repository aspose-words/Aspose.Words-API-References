---
title: BookmarkCollection Class
linktitle: BookmarkCollection
articleTitle: BookmarkCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.BookmarkCollection, una poderosa herramienta para administrar marcadores en sus documentos, mejorando la organización y la navegación.
type: docs
weight: 240
url: /es/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

Una colección de[`Bookmark`](../bookmark/) objetos que representan los marcadores en el rango especificado.

Para obtener más información, visite el[Trabajar con marcadores](https://docs.aspose.com/words/net/working-with-bookmarks/) Artículo de documentación.

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | Devuelve el número de marcadores en la colección. |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | Devuelve un marcador en el índice especificado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | Elimina todos los marcadores de esta colección y del documento. |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | Devuelve un objeto enumerador. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(*[Bookmark](../bookmark/)*) | Elimina el marcador especificado del documento. |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(*string*) | Elimina un marcador con el nombre especificado. |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(*int*) | Elimina un marcador en el índice especificado. |

## Ejemplos

Muestra cómo agregar marcadores y actualizar su contenido.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Cree un documento con tres marcadores y luego utilice una implementación de visitante de documento personalizada para imprimir su contenido.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    //Se puede acceder a los marcadores en la colección de marcadores por índice o nombre, y sus nombres se pueden actualizar.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Imprima todos los marcadores nuevamente para ver los valores actualizados.
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// Crea un documento con un número determinado de marcadores.
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// Utilice un iterador y un visitante para imprimir información de cada marcador de la colección.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Obtenga cada marcador de la colección para aceptar un visitante que imprimirá su contenido.
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// Imprime el contenido de cada marcador visitado en la consola.
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### Ver también

* class [Bookmark](../bookmark/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
