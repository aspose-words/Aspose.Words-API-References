---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words för .NET
description: Upptäck egenskapen för teckensnittet DoubleStrikeThrough. Formatera enkelt text med en dubbel genomstrykning för ökad tydlighet och stil i dina dokument.
type: docs
weight: 90
url: /sv/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

Sant om teckensnittet är formaterat som dubbel genomstruken text.

```csharp
public bool DoubleStrikeThrough { get; set; }
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
