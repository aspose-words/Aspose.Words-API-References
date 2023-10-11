---
title: ChartAxisTitle.Text
second_title: Aspose.Words för .NET API Referens
description: ChartAxisTitle fast egendom. Hämtar eller ställer in texten i axeltiteln. Omnull eller tomt värde anges kommer automatiskt genererad titel att visas.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Hämtar eller ställer in texten i axeltiteln. Om`null` eller tomt värde anges, kommer automatiskt genererad titel att visas.

```csharp
public string Text { get; set; }
```

### Anmärkningar

Använda sig av[`Show`](../show/) alternativet om du behöver visa titeln.

### Exempel

Visar hur man ställer in diagramaxelns titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Ta bort standardgenererade serier.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Ställ in axeltitel.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Se även

* class [ChartAxisTitle](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* hopsättning [Aspose.Words](../../../)


