---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ChartAxisCollection, din lösning för att hantera diagramaxlar effektivt och förbättra datavisualiseringen i ditt dokument.
type: docs
weight: 900
url: /sv/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Representerar en samling diagramaxlar.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Hämtar antalet axlar i denna samling. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Hämtar axeln vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |

## Exempel

Visar hur man arbetar med axlar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Dölj de viktigaste rutnätslinjerna på den primära och sekundära Y-axeln.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Se även

* class [ChartAxis](../chartaxis/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
