---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words per .NET
description: PageRange costruttore. Crea un nuovo oggetto intervallo di pagine in C#.
type: docs
weight: 10
url: /it/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

Crea un nuovo oggetto intervallo di pagine.

```csharp
public PageRange(int from, int to)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| from | Int32 | L'indice in base zero della pagina iniziale. |
| to | Int32 | L'indice in base zero della pagina finale. Se supera l'indice dell'ultima pagina del documento, viene troncato per adattarsi al documento durante il rendering. |

## Osservazioni

MaxValue significa l'ultima pagina del documento.

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

* class [PageRange](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
