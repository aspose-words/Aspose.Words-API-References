---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Entdecken Sie die Schriftarteigenschaft „ChartDataLabel“, um die Schriftformatierung Ihres Datenlabels einfach anzupassen und so die Optik und Klarheit zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Bietet Zugriff auf die Schriftformatierung dieses Datenlabels.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
