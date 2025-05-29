---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için ChartDataLabelCollection Font özelliğiyle tüm serilerinizin veri etiketlerinin yazı tipi biçimlendirmesine erişin ve özelleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

Tüm serinin veri etiketlerinin yazı tipi biçimlendirmesine erişim sağlar.

```csharp
public Font Font { get; }
```

## Notlar

Bu özellik için tanımlanan değer, kullanılarak ayrı bir veri etiketi için geçersiz kılınabilir[`Font`](../../chartdatalabel/font/) mülk.

## Örnekler

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

// X ekseni için kategori olarak ayları içeren özel bir grafik serisi ekleyin,
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

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
