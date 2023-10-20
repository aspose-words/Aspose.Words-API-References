---
title: Chart.Axes
linktitle: Axes
articleTitle: Axes
second_title: Aspose.Words för .NET
description: Chart Axes fast egendom. Får en samling av alla axlar i detta diagram i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Får en samling av alla axlar i detta diagram.

```csharp
public ChartAxisCollection Axes { get; }
```

## Exempel

Visar hur man arbetar med yxsamling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Göm de stora rutnätslinjerna på den primära och sekundära Y-axeln.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Se även

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
