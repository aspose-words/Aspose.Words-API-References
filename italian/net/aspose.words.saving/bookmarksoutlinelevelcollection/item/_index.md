---
title: Item
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta un livello di struttura del segnalibro in base al nome del segnalibro.
type: docs
weight: 30
url: /it/net/aspose.words.saving/bookmarksoutlinelevelcollection/item/
---
## BookmarksOutlineLevelCollection indexer (1 of 2)

Ottiene o imposta un livello di struttura del segnalibro in base al nome del segnalibro.

```csharp
public int this[string name] { get; set; }
```

| Parametro | Descrizione |
| --- | --- |
| name | Nome del segnalibro senza distinzione tra maiuscole e minuscole. |

### Valore di ritorno

Il livello di struttura del segnalibro. L'intervallo valido è compreso tra 0 e 9.

### Esempi

Mostra come impostare i livelli di struttura per i segnalibri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un segnalibro con un altro segnalibro nidificato al suo interno.
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

// Quando si salva in .pdf, è possibile accedere ai segnalibri tramite un menu a discesa e utilizzarli come ancoraggi dalla maggior parte dei lettori.
// I segnalibri possono anche avere valori numerici per i livelli di struttura,
// abilita le voci della struttura di livello inferiore per nascondere le voci secondarie di livello superiore quando vengono compresse nel lettore.
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

// Ci sono nove livelli di struttura. La loro numerazione sarà ottimizzata durante l'operazione di salvataggio.
// In questo caso, i livelli "5" e "9" diventeranno "2" e "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Lo svuotamento di questa raccolta conserverà i segnalibri e li metterà tutti sullo stesso livello di struttura.
outlineLevels.Clear();
```

### Guarda anche

* class [BookmarksOutlineLevelCollection](../../bookmarksoutlinelevelcollection)
* spazio dei nomi [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection)
* assemblea [Aspose.Words](../../../)

---

## BookmarksOutlineLevelCollection indexer (2 of 2)

Ottiene o imposta un livello di struttura del segnalibro all'indice specificato.

```csharp
public int this[int index] { get; set; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice in base zero del segnalibro. |

### Valore di ritorno

Il livello di struttura del segnalibro. L'intervallo valido è compreso tra 0 e 9.

### Esempi

Mostra come impostare i livelli di struttura per i segnalibri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un segnalibro con un altro segnalibro nidificato al suo interno.
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

// Quando si salva in .pdf, è possibile accedere ai segnalibri tramite un menu a discesa e utilizzarli come ancoraggi dalla maggior parte dei lettori.
// I segnalibri possono anche avere valori numerici per i livelli di struttura,
// abilita le voci della struttura di livello inferiore per nascondere le voci secondarie di livello superiore quando vengono compresse nel lettore.
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

// Ci sono nove livelli di struttura. La loro numerazione sarà ottimizzata durante l'operazione di salvataggio.
// In questo caso, i livelli "5" e "9" diventeranno "2" e "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Lo svuotamento di questa raccolta conserverà i segnalibri e li metterà tutti sullo stesso livello di struttura.
outlineLevels.Clear();
```

### Guarda anche

* class [BookmarksOutlineLevelCollection](../../bookmarksoutlinelevelcollection)
* spazio dei nomi [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
