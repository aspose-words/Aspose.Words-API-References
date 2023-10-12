---
title: Class BookmarksOutlineLevelCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.BookmarksOutlineLevelCollection classe. Una raccolta di singoli segnalibri a livello di struttura.
type: docs
weight: 4850
url: /it/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

Una raccolta di singoli segnalibri a livello di struttura.

Per saperne di più, visita il[Lavorare con i segnalibri](https://docs.aspose.com/words/net/working-with-bookmarks/) articolo di documentazione.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Ottiene o imposta un livello di struttura del segnalibro in base al nome del segnalibro. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(string, int) | Aggiunge un segnalibro alla raccolta. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(string) | Determina se la raccolta contiene un segnalibro con il nome specificato. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi della raccolta. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(string) | Restituisce l'indice in base zero del segnalibro specificato nella raccolta. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(string) | Rimuove un segnalibro con il nome specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(int) | Rimuove un segnalibro all'indice specificato. |

### Osservazioni

Key è un nome di segnalibro stringa senza distinzione tra maiuscole e minuscole. Il valore è un livello di struttura del segnalibro int.

Il livello della struttura del segnalibro può essere un valore compreso tra 0 e 9. Specifica 0 e il segnalibro di Word non verrà visualizzato nella struttura del documento. Specifica 1 e il segnalibro di Word verrà visualizzato nella struttura del documento al livello 1; 2 per il livello 2 e così via.

### Esempi

Mostra come impostare i livelli di struttura per i segnalibri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un segnalibro con un altro segnalibro nidificato al suo interno.
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
// abilita le voci di struttura di livello inferiore per nascondere le voci secondarie di livello superiore quando vengono compresse nel lettore.
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

// Lo svuotamento di questa raccolta conserverà i segnalibri e li metterà tutti sullo stesso livello di struttura.
outlineLevels.Clear();
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


