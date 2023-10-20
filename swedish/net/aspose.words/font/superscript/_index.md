---
title: Font.Superscript
linktitle: Superscript
articleTitle: Superscript
second_title: Aspose.Words för .NET
description: Font Superscript fast egendom. Sant om teckensnittet är formaterat som upphöjt i C#.
type: docs
weight: 440
url: /sv/net/aspose.words/font/superscript/
---
## Font.Superscript property

Sant om teckensnittet är formaterat som upphöjt.

```csharp
public bool Superscript { get; set; }
```

## Exempel

Visar hur man formaterar text för att förskjuta dess position.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Höj den här texten 5 punkter över baslinjen.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Sänk denna textserie 10 punkter under baslinjen.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Lägg till en serie normal text.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Lägg till en serie text som visas som nedsänkt.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Lägg till en serie text som visas som upphöjd.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
