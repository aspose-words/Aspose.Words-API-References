---
title: ChartAxis.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartAxis Title-Eigenschaft für einfachen Zugriff und Anpassung von Achsentiteln und verbessern Sie so Ihre Datenvisualisierung und -präsentation.
type: docs
weight: 250
url: /de/net/aspose.words.drawing.charts/chartaxis/title/
---
## ChartAxis.Title property

Bietet Zugriff auf die Achsentiteleigenschaften.

```csharp
public ChartAxisTitle Title { get; }
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

* class [ChartAxisTitle](../../chartaxistitle/)
* class [ChartAxis](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
