---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartAxisTitle sınıf. Eksen başlığı özelliklerine erişim sağlar C#'da.
type: docs
weight: 650
url: /tr/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Eksen başlığı özelliklerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[ Grafikleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartAxisTitle
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Diğer grafik öğelerinin başlıkla çakışmasına izin verilip verilmeyeceğini belirler. Varsayılan değer:`YANLIŞ` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Eksen için başlığın gösterilip gösterilmeyeceğini belirler. Varsayılan değer:`YANLIŞ` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Eksen başlığının metnini alır veya ayarlar. If`hükümsüz` veya boş değer belirtilirse otomatik oluşturulan başlık gösterilecektir. |

## Örnekler

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
