---
title: Chart.DataTable
linktitle: DataTable
articleTitle: DataTable
second_title: .NET için Aspose.Words
description: Grafiğinizin DataTable özelliklerine zahmetsizce erişin ve özelleştirin. Net içgörüler için Göster özelliğiyle veri görselleştirmesini geliştirin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chart/datatable/
---
## Chart.DataTable property

Bu grafiğin veri tablosunun özelliklerine erişim sağlar. Veri tablosu, kullanılarak gösterilebilir.[`Show`](../../chartdatatable/show/) mülk.

```csharp
public ChartDataTable DataTable { get; }
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

* class [ChartDataTable](../../chartdatatable/)
* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
