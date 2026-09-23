---
title: "PageRange"
linktitle: "PageRange"
second_title: "Aspose.Words pour Java"
description: "Représente une plage continue de pages en Java."
type: docs
weight: 516
url: /fr/java/com.aspose.words/pagerange/
---

**Inheritance:**
java.lang.Object
```
public class PageRange
```

Représente une plage continue de pages.

Pour en savoir plus, consultez l'article de documentation [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Montre comment extraire des pages en fonction de plages de pages exactes.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Constructors

| Constructor | Description |
| --- | --- |
| [PageRange(int from, int to)](#PageRange-int-int) | Crée un nouvel objet de plage de pages. |
### PageRange(int from, int to) {#PageRange-int-int}
```
public PageRange(int from, int to)
```


Crée un nouvel objet de plage de pages.

 **Remarks:** 

**Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

Montre comment extraire des pages en fonction de plages de pages exactes.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| de | int | L'index de page de départ basé sur zéro. |
| à | int | L'index de page de fin basé sur zéro. S'il dépasse l'index de la dernière page du document, il est tronqué pour s'adapter au document lors du rendu. |

