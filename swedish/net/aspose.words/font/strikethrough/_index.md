---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words för .NET
description: Upptäck egenskapen för genomstruken text. Formatera enkelt text med genomstruken text för tydlig visuell betoning i dina designer. Förbättra läsbarheten idag!
type: docs
weight: 400
url: /sv/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Sant om teckensnittet är formaterat som genomstruken text.

```csharp
public bool StrikeThrough { get; set; }
```

## Exempel

Visar hur man lägger till en genomstrykning av text.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
