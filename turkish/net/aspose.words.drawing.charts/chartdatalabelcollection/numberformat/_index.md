---
title: ChartDataLabelCollection.NumberFormat
second_title: Aspose.Words for .NET API Referansı
description: ChartDataLabelCollection mülk. Bir alırChartNumberFormat the serisinin tamamının veri etiketleri için sayı formatını ayarlamaya izin veren örnek.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Bir alır[`ChartNumberFormat`](../../chartnumberformat/) the serisinin tamamının veri etiketleri için sayı formatını ayarlamaya izin veren örnek.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### Örnekler

Bir grafik serisi için veri etiketlerinin nasıl etkinleştirileceğini ve yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir çizgi grafiği ekleyin, ardından temiz bir grafikle başlamak için demo veri serisini temizleyin,
// ve ardından bir başlık belirleyin.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// X ekseni için ayları kategoriler halinde içeren özel bir grafik serisi ekleyin,
// ve Y ekseni için ilgili ondalık miktarlar.
ChartSeries series = chart.Series.Add("Revenue", 
    new[] { "January", "February", "March" }, 
    new[] { 25.611d, 21.439d, 33.750d });

// Veri etiketlerini etkinleştirin ve ardından veri etiketlerinde görüntülenen değerler için özel bir sayı biçimi uygulayın.
// Bu format, görüntülenen ondalık değerleri milyonlarca ABD Doları olarak ele alacaktır.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;            

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### Ayrıca bakınız

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* toplantı [Aspose.Words](../../../)


