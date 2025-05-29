---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Font Border, som erbjuder ett anpassningsbart Border-objekt för att förbättra din flexibilitet inom teckensnittsstil och design.
type: docs
weight: 60
url: /sv/net/aspose.words/font/border/
---
## Font.Border property

Returnerar en[`Border`](../../border/) objekt som anger ramen för teckensnittet.

```csharp
public Border Border { get; }
```

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

* class [Border](../../border/)
* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
