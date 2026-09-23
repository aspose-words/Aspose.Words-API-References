---
title: "PageRange"
linktitle: "PageRange"
second_title: "Aspose.Words für Java"
description: "Stellt einen zusammenhängenden Seitenbereich in Java dar."
type: docs
weight: 516
url: /de/java/com.aspose.words/pagerange/
---

**Inheritance:**
java.lang.Object
```
public class PageRange
```

Stellt einen zusammenhängenden Seitenbereich dar.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Zeigt, wie man Seiten basierend auf genauen Seitenbereichen extrahiert.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [PageRange(int from, int to)](#PageRange-int-int) | Erstellt ein neues Seitenbereichs‑Objekt. |
### PageRange(int from, int to) {#PageRange-int-int}
```
public PageRange(int from, int to)
```


Erstellt ein neues Seitenbereichs‑Objekt.

 **Remarks:** 

**Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

Zeigt, wie man Seiten basierend auf genauen Seitenbereichen extrahiert.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| von | int | Der nullbasierte Index der Startseite. |
| bis | int | Der nullbasierte Index der Endseite. Überschreitet er den Index der letzten Seite im Dokument, wird er beim Rendern auf die Dokumentgröße gekürzt. |

