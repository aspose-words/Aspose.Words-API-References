---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words per .NET
description: Crea intervalli di pagine personalizzati senza sforzo con il nostro costruttore PageRange. Migliora la gestione dei tuoi documenti con precisione e flessibilità.
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
| from | Int32 | Indice a base zero della pagina iniziale. |
| to | Int32 | Indice di pagina finale basato su zero. Se supera l'indice dell'ultima pagina del documento, viene troncato per adattarlo al documento durante il rendering. |

## Osservazioni

MaxValue indica l'ultima pagina del documento.

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
