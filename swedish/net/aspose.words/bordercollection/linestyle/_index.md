---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words för .NET
description: BorderCollection LineStyle fast egendom. Hämtar eller ställer in kantstilen i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Hämtar eller ställer in kantstilen.

```csharp
public LineStyle LineStyle { get; set; }
```

## Anmärkningar

Returnerar stilen för den första kanten i samlingen.

Ställer in stilen för alla kanter i samlingen exklusive diagonala kanter.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
