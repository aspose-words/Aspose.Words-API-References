---
title: Font.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: Aspose.Words för .NET
description: Upptäck egenskapen för teckensnitt med små versaler. Formatera enkelt text med små bokstäver för förbättrad läsbarhet och ett snyggt utseende i dina designer.
type: docs
weight: 370
url: /sv/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

Sant om teckensnittet är formaterat som små versaler.

```csharp
public bool SmallCaps { get; set; }
```

## Exempel

Visar hur man formaterar en körning för att visa innehållet med versaler.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Det finns två sätt att få en körning att visa sin gemena text i versaler utan att ändra innehållet.
// 1 - Ställ in flaggan AllCaps för att visa alla tecken med vanliga versaler:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Ställ in SmallCaps-flaggan för att visa alla tecken med små versaler:
// Om ett tecken är gement, visas det med versaler
// men kommer att ha samma höjd som gemenerna (teckensnittets x-höjd).
// Tecken som ursprungligen var skrivna med versaler kommer att se likadana ut.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
