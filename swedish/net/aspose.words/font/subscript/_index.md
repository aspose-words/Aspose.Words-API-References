---
title: Font.Subscript
second_title: Aspose.Words för .NET API Referens
description: Font fast egendom. True om teckensnittet är formaterat som subscript.
type: docs
weight: 430
url: /sv/net/aspose.words/font/subscript/
---
## Font.Subscript property

True om teckensnittet är formaterat som subscript.

```csharp
public bool Subscript { get; set; }
```

### Exempel

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
* namnutrymme [Aspose.Words](../../font/)
* hopsättning [Aspose.Words](../../../)


