---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words för .NET
description: Font HighlightColor fast egendom. Hämtar eller ställer in markeringsfärgen i C#.
type: docs
weight: 150
url: /sv/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Hämtar eller ställer in markeringsfärgen.

```csharp
public Color HighlightColor { get; set; }
```

## Exempel

Visar hur man formaterar en serie text med dess teckensnittsegenskap.

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
