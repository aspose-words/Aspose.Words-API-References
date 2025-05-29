---
title: BookmarkCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words para .NET
description: Administre sin esfuerzo sus marcadores con el método RemoveAt: ¡elimine rápidamente cualquier marcador por su índice para tener una colección optimizada!
type: docs
weight: 60
url: /es/net/aspose.words/bookmarkcollection/removeat/
---
## BookmarkCollection.RemoveAt method

Elimina un marcador en el índice especificado.

```csharp
public void RemoveAt(int index)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice basado en cero del marcador que se eliminará. |

## Ejemplos

Muestra cómo eliminar marcadores de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta cinco marcadores con texto dentro de sus límites.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

//Esta colección almacena marcadores.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

//Hay varias formas de eliminar marcadores.
// 1 - Llamar al método Remove del marcador:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Pasando el marcador al método Remove de la colección:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Eliminar un marcador de la colección por nombre:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Eliminar un marcador en un índice de la colección de marcadores:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

//Podemos borrar toda la colección de marcadores.
bookmarks.Clear();

//El texto que estaba dentro de los marcadores todavía está presente en el documento.
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Ver también

* class [BookmarkCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
