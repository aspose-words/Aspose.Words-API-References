---
title: Bookmark.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi facilmente i segnalibri dal tuo documento, preservando il testo al suo interno. Semplifica il tuo processo di modifica con il nostro efficiente metodo di rimozione dei segnalibri!
type: docs
weight: 80
url: /it/net/aspose.words/bookmark/remove/
---
## Bookmark.Remove method

Rimuove il segnalibro dal documento. Non rimuove il testo all'interno del segnalibro.

```csharp
public void Remove()
```

## Esempi

Mostra come rimuovere i segnalibri da un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire cinque segnalibri con il testo all'interno dei rispettivi margini.
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
// 1 - Chiamata del metodo Remove del segnalibro:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - Passaggio del segnalibro al metodo Remove della raccolta:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - Rimozione di un segnalibro dalla raccolta in base al nome:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - Rimozione di un segnalibro da un indice nella raccolta dei segnalibri:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// Possiamo cancellare l'intera raccolta di segnalibri.
bookmarks.Clear();

// Il testo presente nei segnalibri è ancora presente nel documento.
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### Guarda anche

* class [Bookmark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
