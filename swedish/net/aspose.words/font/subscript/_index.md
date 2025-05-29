---
title: Font.Subscript
linktitle: Subscript
articleTitle: Subscript
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Teckensnittsnedsänkning. Formatera enkelt text som nedsänkning för förbättrad läsbarhet och stil i dina dokument. Förbättra din design idag!
type: docs
weight: 440
url: /sv/net/aspose.words/font/subscript/
---
## Font.Subscript property

Sant om teckensnittet är formaterat som nedsänkt skrift.

```csharp
public bool Subscript { get; set; }
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
