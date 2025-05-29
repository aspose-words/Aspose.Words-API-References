---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: .NET için Aspose.Words
description: ChartDataTable Show özelliğiyle grafiğinizin görünürlüğünü kontrol edin. Gelişmiş veri içgörüleri için veri tablosu görüntüsünü kolayca değiştirin. Varsayılan, false.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

Veri tablosunun grafik için gösterilip gösterilmeyeceğini belirten bir bayrak alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool Show { get; set; }
```

## Notlar

Aşağıdaki grafik türleri veri tablolarını desteklemez: Dağılım, Pasta, Çörek, Yüzey, Radar, Ağaç Haritası, Güneş Patlaması, Histogram, Pareto, Kutu ve Bıyık, Şelale, Huni, Bu türlerden oluşan serileri içeren Kombo grafikler. Grafik türleri için bir veri tablosu göstermek bir hataya neden olur.InvalidOperationException istisnası.

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
