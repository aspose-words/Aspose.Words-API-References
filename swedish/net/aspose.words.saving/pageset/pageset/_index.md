---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words för .NET
description: PageSet byggare. Skapar en ensidig uppsättning baserat på exakt sidindex i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Skapar en ensidig uppsättning baserat på exakt sidindex.

```csharp
public PageSet(int page)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| page | Int32 | Nollbaserat index för sidan. |

## Anmärkningar

Om en sida påträffas som inte finns i dokumentet kommer ett undantag att kastas under renderingen. MaxValue betyder den sista sidan i dokumentet.

### Se även

* class [PageSet](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Skapar en siduppsättning baserat på exakta sidindex.

```csharp
public PageSet(params int[] pages)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pages | Int32[] | Nollbaserade index för sidor. |

## Anmärkningar

Om en sida påträffas som inte finns i dokumentet kommer ett undantag att kastas under renderingen. MaxValue betyder den sista sidan i dokumentet.

## Exempel

Visar hur man extraherar sidor baserat på exakta sidindex.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till fem sidor i dokumentet.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Skapa ett "XpsSaveOptions"-objekt, som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Använd egenskapen "PageSet" för att välja en uppsättning av dokumentets sidor att spara till utdata XPS.
// I det här fallet väljer vi, via ett nollbaserat index, endast tre sidor: sida 1, sida 2 och sida 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Se även

* class [PageSet](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Skapar en siduppsättning baserat på intervall.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| ranges | PageRange[] | Uppsättning av sidintervall. |

## Anmärkningar

Om ett intervall påträffas som börjar efter den sista sidan i dokumentet, kommer ett undantag att kastas under renderingen. Alla intervall som slutar efter den sista sidan trunkeras för att passa in i dokumentet.

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
