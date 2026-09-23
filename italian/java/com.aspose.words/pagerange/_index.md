---
title: "PageRange"
linktitle: "PageRange"
second_title: "Aspose.Words per Java"
description: "Rappresenta un intervallo continuo di pagine in Java."
type: docs
weight: 516
url: /it/java/com.aspose.words/pagerange/
---

**Inheritance:**
java.lang.Object
```
public class PageRange
```

Rappresenta un intervallo continuo di pagine.

Per saperne di più, visita l'articolo di documentazione [ Programmare con i Documenti ][Programming with Documents].

 **Examples:** 

Mostra come estrarre pagine basate su intervalli di pagine esatti.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [PageRange(int from, int to)](#PageRange-int-int) | Crea un nuovo oggetto intervallo di pagine. |
### PageRange(int from, int to) {#PageRange-int-int}
```
public PageRange(int from, int to)
```


Crea un nuovo oggetto intervallo di pagine.

 **Remarks:** 

**Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

Mostra come estrarre pagine basate su intervalli di pagine esatti.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| da | int | L'indice della pagina iniziale basato su zero. |
| a | int | L'indice della pagina finale basato su zero. Se supera l'indice dell'ultima pagina del documento, viene troncato per adattarsi al documento durante il rendering. |

