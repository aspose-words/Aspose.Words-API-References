---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words för .NET
description: Anpassa din design med egenskapen Border LineStyle, så att du enkelt kan hämta eller ställa in unika kantstilar för förbättrad visuell tilltalning.
type: docs
weight: 40
url: /sv/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Hämtar eller ställer in kantstilen.

```csharp
public LineStyle LineStyle { get; set; }
```

## Anmärkningar

Om du ställer in linjestilen till ingen ändras linjebredden automatiskt till noll.

## Exempel

Visar hur man infogar en sträng omgiven av en kantlinje i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Se även

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
