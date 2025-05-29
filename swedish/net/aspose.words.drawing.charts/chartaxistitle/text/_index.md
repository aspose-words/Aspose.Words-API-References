---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartAxisTitle Text för att enkelt anpassa dina axeltitlar. Ställ in eller hämta dynamiska titlar för förbättrad datavisualisering.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Hämtar eller ställer in texten i axelrubriken. Om`null` eller om ett tomt värde anges visas den automatiskt genererade titeln.

```csharp
public string Text { get; set; }
```

## Anmärkningar

Använda[`Show`](../show/)alternativ om du behöver visa titeln.

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

* class [ChartAxisTitle](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
