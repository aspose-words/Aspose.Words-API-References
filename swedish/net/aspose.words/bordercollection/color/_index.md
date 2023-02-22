---
title: BorderCollection.Color
second_title: Aspose.Words för .NET API Referens
description: BorderCollection fast egendom. Hämtar eller ställer in kantfärgen.
type: docs
weight: 20
url: /sv/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Hämtar eller ställer in kantfärgen.

```csharp
public Color Color { get; set; }
```

### Anmärkningar

Returnerar färgen på den första kanten i samlingen.

Ställer in färgen på alla ramar i samlingen exklusive diagonala kanter.

### Exempel

Visar hur man skapar grön vågig sidkant med en skugga.

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
* namnutrymme [Aspose.Words](../../bordercollection/)
* hopsättning [Aspose.Words](../../../)


