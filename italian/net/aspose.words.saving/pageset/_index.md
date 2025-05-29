---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.PageSet per una gestione efficiente dei documenti. Definisci facilmente set di pagine casuali e migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 6170
url: /it/net/aspose.words.saving/pageset/
---
## PageSet class

Descrive un insieme casuale di pagine.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Crea un set di una pagina basato sull'indice di pagina esatto. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Crea un set di pagine basato sugli indici di pagina esatti. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Crea un set di pagine basato su intervalli. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Ottiene un set con tutte le pagine del documento nel loro ordine originale. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Ottiene un set con tutte le pagine pari del documento nel loro ordine originale. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Ottiene un set con tutte le pagine dispari del documento nel loro ordine originale. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## Esempi

Mostra come convertire una pagina di un documento in un'immagine JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Creiamo un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo trasforma il documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Imposta "PageSet" su "1" per selezionare la seconda pagina tramite
// l'indice a partire da zero da cui iniziare il rendering del documento.
options.PageSet = new PageSet(1);

// Quando salviamo il documento nel formato JPEG, Aspose.Words esegue il rendering di una sola pagina.
// Questa immagine conterrà una pagina a partire da pagina due,
// che sarà semplicemente la seconda pagina del documento originale.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
