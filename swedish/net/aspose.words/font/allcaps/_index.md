---
title: Font.AllCaps
linktitle: AllCaps
articleTitle: AllCaps
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font AllCaps. Formatera enkelt text med versaler för förbättrad läsbarhet och effektfull design i dina projekt.
type: docs
weight: 10
url: /sv/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Sant om teckensnittet är formaterat med enbart versaler.

```csharp
public bool AllCaps { get; set; }
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
