---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Teckensnittsposition, justera enkelt textjusteringen i punkter för exakt kontroll över din typografi. Förhöj din design med flexibel positionering!
type: docs
weight: 310
url: /sv/net/aspose.words/font/position/
---
## Font.Position property

Hämtar eller ställer in textens position (i punkter) i förhållande till baslinjen. Ett positivt tal höjer texten och ett negativt tal sänker den.

```csharp
public double Position { get; set; }
```

## Exempel

Visar hur man formaterar text för att förskjuta dess position.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Höj denna textsekvens 5 punkter över baslinjen.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Sänk denna textsekvens 10 punkter under baslinjen.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Lägg till en sekvens med vanlig text.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Lägg till en textsekvens som visas som nedsänkt skrift.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Lägg till en textsekvens som visas som upphöjd skrift.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
