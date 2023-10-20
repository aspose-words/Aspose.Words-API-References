---
title: Chart.Axes
linktitle: Axes
articleTitle: Axes
second_title: Aspose.Words für .NET
description: Chart Axes eigendom. Ruft eine Sammlung aller Achsen dieses Diagramms ab in C#.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Ruft eine Sammlung aller Achsen dieses Diagramms ab.

```csharp
public ChartAxisCollection Axes { get; }
```

## Beispiele

Zeigt, wie man mit der Achsensammlung arbeitet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Die Hauptgitterlinien auf der primären und sekundären Y-Achse ausblenden.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Siehe auch

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
