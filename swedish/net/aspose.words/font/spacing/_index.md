---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Teckenavstånd för att enkelt justera teckenavståndet i punkter. Förbättra läsbarhet och design med exakt typografisk kontroll.
type: docs
weight: 390
url: /sv/net/aspose.words/font/spacing/
---
## Font.Spacing property

Returnerar eller anger avståndet (i punkter) mellan tecken.

```csharp
public double Spacing { get; set; }
```

## Exempel

Visar hur man ställer in horisontell skalning och avstånd för tecken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till textlängd och öka teckenbredden till 150 %.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Lägg till textlängd och lägg till 1 pt extra horisontellt avstånd mellan varje tecken.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Lägg till textlängd och för tecknen närmare varandra med 1 pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
