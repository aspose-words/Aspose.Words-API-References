---
title: Bookmark.Remove
second_title: Aspose.Words per .NET API Reference
description: Bookmark metodo. Rimuove il segnalibro dal documento. Non rimuove il testo allinterno del segnalibro.
type: docs
weight: 80
url: /it/net/aspose.words/bookmark/remove/
---
## Bookmark.Remove method

Rimuove il segnalibro dal documento. Non rimuove il testo all'interno del segnalibro.

```csharp
public void Remove()
```

### Esempi

Mostra come rimuovere i segnalibri da un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci cinque segnalibri con il testo all'interno dei loro limiti.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// Questa raccolta memorizza i segnalibri.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// Esistono diversi modi per rimuovere i segnalibri.
// 1 - Chiamare il metodo Rimuovi del segnalibro:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Passaggio del segnalibro al metodo Rimuovi della raccolta:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Rimozione di un segnalibro dalla raccolta per nome:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Rimozione di un segnalibro in un indice nella raccolta di segnalibri:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Possiamo cancellare l'intera raccolta di segnalibri.
bookmarks.Clear();

// Il testo che era all'interno dei segnalibri è ancora presente nel documento.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Guarda anche

* class [Bookmark](../)
* spazio dei nomi [Aspose.Words](../../bookmark/)
* assemblea [Aspose.Words](../../../)


