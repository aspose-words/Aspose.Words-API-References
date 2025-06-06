---
title: ChartSeries.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Blasendiagramm mit ChartSeries Bubble3D! Fügen Sie Ihren Blasen atemberaubende 3D-Effekte hinzu und erzielen Sie so eine beeindruckende visuelle Wirkung.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartseries/bubble3d/
---
## ChartSeries.Bubble3D property

Gibt an, ob auf die Blasen im Blasendiagramm ein 3D-Effekt angewendet werden soll.

```csharp
public bool Bubble3D { get; set; }
```

## Beispiele

Zeigt, wie 3D-Effekte mit Blasendiagrammen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Wenden Sie auf jede Blase eine Datenbeschriftung an, die ihren Durchmesser anzeigt.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Siehe auch

* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
