---
title: ChartAxisTitle.Show
second_title: Aspose.Words for .NET API Referansı
description: ChartAxisTitle mülk. Eksen için başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değerYANLIŞ .
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

Eksen için başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değer:`YANLIŞ` .

```csharp
public bool Show { get; set; }
```

### Örnekler

Grafik ekseni başlığının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Varsayılan olarak oluşturulan seriyi silin.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Eksen başlığını ayarlayın.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Ayrıca bakınız

* class [ChartAxisTitle](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* toplantı [Aspose.Words](../../../)


