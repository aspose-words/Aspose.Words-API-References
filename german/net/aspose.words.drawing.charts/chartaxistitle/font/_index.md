---
title: ChartAxisTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Passen Sie Ihren ChartAxisTitle mit vielseitigen Schriftarten an. Verbessern Sie Ihre Datenvisualisierung mit einer einzigartigen Achsentitelformatierung für klarere Einblicke.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartaxistitle/font/
---
## ChartAxisTitle.Font property

Bietet Zugriff auf die Schriftformatierung des Achsentitels.

```csharp
public Font Font { get; }
```

## Beispiele

Zeigt, wie der Achsentitel eines Diagramms festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Siehe auch

* class [Font](../../../aspose.words/font/)
* class [ChartAxisTitle](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
