---
title: BookmarkEnd.Accept
second_title: Referencia de API de Aspose.Words para .NET
description: BookmarkEnd método. Acepta un visitante.
type: docs
weight: 40
url: /es/net/aspose.words/bookmarkend/accept/
---
## BookmarkEnd.Accept method

Acepta un visitante.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante que visitará el nodo. |

### Valor_devuelto

Falso si el visitante solicitó que se detuviera la enumeración.

### Observaciones

Llamadas[`VisitBookmarkEnd`](../../documentvisitor/visitbookmarkend/).

Para obtener más información, consulte el patrón de diseño Visitante.

### Ejemplos

Muestra cómo agregar marcadores y actualizar su contenido.

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // Cree un documento con tres marcadores, luego use una implementación de visitante de documentos personalizada para imprimir su contenido.
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // Se puede acceder a los marcadores en la colección de marcadores por índice o nombre, y sus nombres se pueden actualizar.
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // Imprime todos los marcadores de nuevo para ver los valores actualizados.
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
/// Use un iterador y un visitante para imprimir información de cada marcador en la colección.
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // Obtenga cada marcador en la colección para aceptar un visitante que imprimirá su contenido.
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

* class [DocumentVisitor](../../documentvisitor/)
* class [BookmarkEnd](../)
* espacio de nombres [Aspose.Words](../../bookmarkend/)
* asamblea [Aspose.Words](../../../)


