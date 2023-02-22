---
title: Font.HighlightColor
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. Hämtar eller ställer in markeringsfärgen.
type: docs
weight: 150
url: /sv/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Hämtar eller ställer in markeringsfärgen.

```csharp
public Color HighlightColor { get; set; }
```

### Exempel

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
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


