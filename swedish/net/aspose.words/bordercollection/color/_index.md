---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BorderCollection Color för att enkelt anpassa och hantera kantfärger för dina designer. Förbättra ditt användargränssnitt med livfulla alternativ!
type: docs
weight: 20
url: /sv/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Hämtar eller ställer in kantfärgen.

```csharp
public Color Color { get; set; }
```

## Anmärkningar

Returnerar färgen på den första kantlinjen i samlingen.

Anger färgen på alla ramar i samlingen exklusive diagonala ramar.

## Exempel

Visar hur man skapar en grön vågig sidkantlinje med en skugga.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Se även

* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
