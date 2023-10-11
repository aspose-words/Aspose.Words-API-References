---
title: Chart.Axes
second_title: Aspose.Words für .NET-API-Referenz
description: Chart eigendom. Ruft eine Sammlung aller Achsen dieses Diagramms ab.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Ruft eine Sammlung aller Achsen dieses Diagramms ab.

```csharp
public ChartAxisCollection Axes { get; }
```

### Beispiele

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
* namensraum [Aspose.Words.Drawing.Charts](../../chart/)
* Montage [Aspose.Words](../../../)


