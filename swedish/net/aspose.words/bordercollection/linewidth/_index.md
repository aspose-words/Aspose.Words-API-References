---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words för .NET
description: BorderCollection LineWidth fast egendom. Hämtar eller ställer in kantbredden i punkter i C#.
type: docs
weight: 90
url: /sv/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Hämtar eller ställer in kantbredden i punkter.

```csharp
public double LineWidth { get; set; }
```

## Anmärkningar

Returnerar bredden på den första kanten i samlingen.

Ställer in bredden på alla kanter i samlingen exklusive diagonala kanter.

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
