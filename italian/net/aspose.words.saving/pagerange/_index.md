---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.PageRange per definire facilmente intervalli di pagine continui. Migliora l'elaborazione dei tuoi documenti con precisione ed efficienza.
type: docs
weight: 6150
url: /it/net/aspose.words.saving/pagerange/
---
## PageRange class

Rappresenta un intervallo continuo di pagine.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public sealed class PageRange
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Crea un nuovo oggetto intervallo di pagine. |

## Esempi

Mostra come estrarre le pagine in base a intervalli di pagine esatti.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
