---
title: Border.LineStyle
second_title: Aspose.Words för .NET API Referens
description: Border fast egendom. Hämtar eller ställer in kantstilen.
type: docs
weight: 40
url: /sv/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Hämtar eller ställer in kantstilen.

```csharp
public LineStyle LineStyle { get; set; }
```

### Anmärkningar

Om du ställer in linjestil till ingen, ändras linjebredden automatiskt till noll.

### Exempel

Visar hur man infogar en sträng omgiven av en kant i ett dokument.

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
* namnutrymme [Aspose.Words](../../border/)
* hopsättning [Aspose.Words](../../../)


