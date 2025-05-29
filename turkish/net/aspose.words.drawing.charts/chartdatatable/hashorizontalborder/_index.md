---
title: ChartDataTable.HasHorizontalBorder
linktitle: HasHorizontalBorder
articleTitle: HasHorizontalBorder
second_title: .NET için Aspose.Words
description: Veri tablonuzun görünümünü kolayca özelleştirmek için ChartDataTable HasHorizontalBorder özelliğini keşfedin. Gelişmiş görsel netlik için yatay kenarlıkları kontrol edin!
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartdatatable/hashorizontalborder/
---
## ChartDataTable.HasHorizontalBorder property

Veri tablosunun yatay kenarlığının görüntülenip görüntülenmeyeceğini belirten bir bayrak alır veya ayarlar. Varsayılan değer`doğru` .

```csharp
public bool HasHorizontalBorder { get; set; }
```

## Örnekler

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Ayrıca bakınız

* class [ChartDataTable](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
