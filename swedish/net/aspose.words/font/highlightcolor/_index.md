---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font HighlightColor – anpassa enkelt textens markeringsfärg för förbättrad läsbarhet och visuell attraktionskraft. Förhöj din design!
type: docs
weight: 150
url: /sv/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Hämtar eller ställer in markeringsfärgen (markörfärgen).

```csharp
public Color HighlightColor { get; set; }
```

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

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
