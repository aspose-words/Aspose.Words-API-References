---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.PageRange för att enkelt definiera kontinuerliga sidintervall. Förbättra din dokumentbehandling med precision och effektivitet.
type: docs
weight: 6150
url: /sv/net/aspose.words.saving/pagerange/
---
## PageRange class

Representerar ett kontinuerligt sidintervall.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public sealed class PageRange
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Skapar ett nytt sidintervallobjekt. |

## Exempel

Visar hur man extraherar sidor baserat på exakta sidintervall.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
