---
title: OutlineOptions.BookmarksOutlineLevels
linktitle: BookmarksOutlineLevels
articleTitle: BookmarksOutlineLevels
second_title: Aspose.Words per .NET
description: Scopri la proprietà BookmarksOutlineLevels in OutlineOptions per personalizzare la gerarchia dei tuoi segnalibri, migliorando la navigazione e l'esperienza utente.
type: docs
weight: 20
url: /it/net/aspose.words.saving/outlineoptions/bookmarksoutlinelevels/
---
## OutlineOptions.BookmarksOutlineLevels property

Consente di specificare il livello di struttura dei singoli segnalibri.

```csharp
public BookmarksOutlineLevelCollection BookmarksOutlineLevels { get; }
```

## Osservazioni

Se il livello del segnalibro non è specificato in questa raccolta, allora[`DefaultBookmarksOutlineLevel`](../defaultbookmarksoutlinelevel/) viene utilizzato il valore.

## Esempi

Mostra come impostare i livelli di struttura per i segnalibri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un segnalibro con un altro segnalibro annidato al suo interno.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Inserisci un altro segnalibro.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// Salvando in formato .pdf, i segnalibri sono accessibili tramite un menu a discesa e possono essere utilizzati come punti di riferimento dalla maggior parte dei lettori.
// I segnalibri possono anche avere valori numerici per i livelli di struttura,
// abilita le voci di struttura di livello inferiore per nascondere le voci figlio di livello superiore quando compresse nel lettore.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// Possiamo rimuovere due elementi in modo che rimanga solo la designazione del livello di struttura per "Segnalibro 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Ci sono nove livelli di struttura. La loro numerazione verrà ottimizzata durante l'operazione di salvataggio.
// In questo caso, i livelli "5" e "9" diventeranno "2" e "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Svuotando questa raccolta i segnalibri verranno conservati e tutti verranno inseriti nello stesso livello di struttura.
outlineLevels.Clear();
```

### Guarda anche

* class [BookmarksOutlineLevelCollection](../../bookmarksoutlinelevelcollection/)
* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
