---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Teckensnittsnamn för att enkelt anpassa och ställa in dina teckensnittsstilar, vilket förbättrar din designs attraktionskraft och läsbarhet.
type: docs
weight: 230
url: /sv/net/aspose.words/font/name/
---
## Font.Name property

Hämtar eller anger namnet på teckensnittet.

```csharp
public string Name { get; set; }
```

## Anmärkningar

När man får returer[`NameAscii`](../nameascii/).

Vid inställning, sätter[`NameAscii`](../nameascii/) ,[`NameBi`](../namebi/) ,[`NameFarEast`](../namefareast/) och[`NameOther`](../nameother/) till det angivna värdet.

## Exempel

Visar hur man formaterar en textsekvens med hjälp av dess font-egenskap.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Visar hur man infogar formaterad text med hjälp av DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange teckensnittsformatering och lägg sedan till text.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
