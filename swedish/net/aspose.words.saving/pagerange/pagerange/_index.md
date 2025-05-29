---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words för .NET
description: Skapa enkelt anpassade sidintervall med vår PageRange-konstruktor. Förbättra din dokumenthantering med precision och flexibilitet.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

Skapar ett nytt sidintervallobjekt.

```csharp
public PageRange(int from, int to)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| from | Int32 | Startsidans nollbaserade index. |
| to | Int32 | Det nollbaserade indexet för den sista sidan. Om det överstiger indexet för den sista sidan i dokumentet, avkortas det för att passa in i dokumentet vid rendering. |

## Anmärkningar

MaxValue betyder den sista sidan i dokumentet.

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

* class [PageRange](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
