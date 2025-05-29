---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words för .NET
description: Styr din dokumentlayout med egenskapen TeckenPerRad i PageSetup. Justera enkelt tecken per rad för optimal läsbarhet och design.
type: docs
weight: 100
url: /sv/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Hämtar eller anger antalet tecken per rad i dokumentrutnätet.

```csharp
public int CharactersPerLine { get; set; }
```

## Anmärkningar

Minsta värde för egenskapen är 1. Maximalt värde beror på sidbredd och teckenstorlek för stilen Normal . Minsta teckenbredd är 90 procent av teckenstorleken. Till exempel är maximalt antal tecken per rad på en Letter-sida med en-tums marginaler 43.

Som standard har egenskapen ett värde där teckenbredd är lika med teckenstorleken för stilen Normal .

## Exempel

Visar hur man anger ett för antalet tecken som varje rad får innehålla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivera radbreddning och använd den sedan för att ange antalet tecken per rad i det här avsnittet.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Antalet tecken beror också på teckenstorleken.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
