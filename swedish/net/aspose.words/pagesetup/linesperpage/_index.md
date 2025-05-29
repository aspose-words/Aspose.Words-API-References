---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words för .NET
description: Styr din dokumentlayout med egenskapen PageSetup LinesPerPage. Justera enkelt rader per sida för optimal läsbarhet och organisation.
type: docs
weight: 240
url: /sv/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Hämtar eller anger antalet rader per sida i dokumentrutnätet.

```csharp
public int LinesPerPage { get; set; }
```

## Anmärkningar

Minsta värde för egenskapen är 1. Maximalt värde beror på sidhöjd och teckenstorlek för stilen Normal . Minsta radavstånd är 136 procent av teckenstorleken. Till exempel är maximalt antal rader per sida på en Letter-sida med en-tums marginaler 39.

Som standard har egenskapen ett värde där radavståndet är 1,5 gånger större än teckenstorleken för i Normal-stilen.

## Exempel

Visar hur man anger en gräns för antalet rader som varje sida får ha.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivera pitching och använd den sedan för att ställa in antalet rader per sida i det här avsnittet.
// En tillräckligt stor teckenstorlek kommer att trycka ner några rader till nästa sida för att undvika överlappande tecken.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
