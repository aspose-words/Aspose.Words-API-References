---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.PageRange zum einfachen Definieren fortlaufender Seitenbereiche. Verbessern Sie Ihre Dokumentenverarbeitung mit Präzision und Effizienz.
type: docs
weight: 6150
url: /de/net/aspose.words.saving/pagerange/
---
## PageRange class

Stellt einen fortlaufenden Seitenbereich dar.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public sealed class PageRange
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Erstellt ein neues Seitenbereichsobjekt. |

## Beispiele

Zeigt, wie Seiten basierend auf genauen Seitenbereichen extrahiert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
