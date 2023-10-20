---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words för .NET
description: Font Spacing fast egendom. Returnerar eller ställer in avståndet i punkter mellan tecknen  i C#.
type: docs
weight: 380
url: /sv/net/aspose.words/font/spacing/
---
## Font.Spacing property

Returnerar eller ställer in avståndet (i punkter) mellan tecknen .

```csharp
public double Spacing { get; set; }
```

## Exempel

Visar hur man ställer in horisontell skalning och avstånd för tecken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till en serie text och öka teckenbredden till 150 %.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Lägg till en serie text och lägg till 1 pkt extra horisontellt mellanrum mellan varje tecken.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Lägg till en rad text och för tecknen närmare varandra med 1 pkt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
