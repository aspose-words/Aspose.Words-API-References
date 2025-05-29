---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: .NET için Aspose.Words
description: Grafik veri tablolarını kolayca özelleştirmek ve güçlü özelliklerle veri görselleştirmenizi geliştirmek için Aspose.Words.Drawing.Charts.ChartDataTable sınıfını keşfedin.
type: docs
weight: 990
url: /tr/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Bir grafik veri tablosunun özelliklerini belirtmeye izin verir.

```csharp
public class ChartDataTable
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Veri tablosunun yazı tipi biçimlendirmesine erişim sağlar. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Veri tablosunun metin arka planının ve kenarlık biçimlendirmesinin doldurulmasına erişim sağlar. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Veri tablosunun yatay kenarlığının görüntülenip görüntülenmeyeceğini belirten bir bayrak alır veya ayarlar. Varsayılan değer`doğru` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Veri tablosunda efsane anahtarlarının görüntülenip görüntülenmeyeceğini belirten bir bayrak alır veya ayarlar. Varsayılan değer`doğru` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Seri ve kategori adları etrafında bir kenarlık olan bir anahat kenarlığının görüntülenip görüntülenmeyeceğini belirten bir bayrak alır veya ayarlar. Varsayılan değer`doğru` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Veri tablosunun dikey kenarlığının görüntülenip görüntülenmeyeceğini belirten bir bayrak alır veya ayarlar. Varsayılan değer`doğru` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Veri tablosunun grafik için gösterilip gösterilmeyeceğini belirten bir bayrak alır veya ayarlar. Varsayılan değer`YANLIŞ` . |

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
