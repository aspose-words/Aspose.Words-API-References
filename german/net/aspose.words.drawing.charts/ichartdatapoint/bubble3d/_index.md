---
title: IChartDataPoint.Bubble3D
second_title: Aspose.Words für .NET-API-Referenz
description: IChartDataPoint eigendom. Gibt an ob auf die Blasen im Blasendiagramm ein 3DEffekt angewendet werden soll.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Gibt an, ob auf die Blasen im Blasendiagramm ein 3D-Effekt angewendet werden soll.

```csharp
public bool Bubble3D { get; set; }
```

### Beispiele

Zeigt, wie 3D-Effekte mit Blasendiagrammen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Wenden Sie ein Datenetikett auf jede Blase an, die ihren Durchmesser anzeigt.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Siehe auch

* interface [IChartDataPoint](../)
* namensraum [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* Montage [Aspose.Words](../../../)


