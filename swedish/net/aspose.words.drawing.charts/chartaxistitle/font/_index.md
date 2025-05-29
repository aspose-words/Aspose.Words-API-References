---
title: ChartAxisTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: Anpassa din ChartAxisTitle med mångsidiga teckensnittsalternativ. Förbättra din datavisualisering med unik axeltitelformatering för tydligare insikter.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartaxistitle/font/
---
## ChartAxisTitle.Font property

Ger åtkomst till teckensnittsformateringen för axeltiteln.

```csharp
public Font Font { get; }
```

## Exempel

Visar hur man ställer in diagramaxelns titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Radera standardgenererad serie.
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

### Se även

* class [Font](../../../aspose.words/font/)
* class [ChartAxisTitle](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
