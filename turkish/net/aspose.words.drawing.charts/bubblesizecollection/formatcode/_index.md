---
title: BubbleSizeCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: .NET için Aspose.Words
description: BubbleSizeCollection FormatCode özelliğini keşfederek baloncuk boyutlarını zahmetsizce özelleştirin. Özelleştirilmiş biçimlendirme seçenekleriyle veri görselleştirmenizi geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/bubblesizecollection/formatcode/
---
## BubbleSizeCollection.FormatCode property

Kabarcık boyutlarına uygulanan biçim kodunu alır veya ayarlar.

```csharp
public string FormatCode { get; set; }
```

## Notlar

Sayı biçimlendirmesi, değerlerin grafikte görünme biçimini değiştirmek için kullanılır. Sayı biçimlerinin örnekleri:

Sayı - "#,##0.00"

Para Birimi - "\"$\"#,##0.00"

Zaman - "[$-x-systime]h:mm:ss AM/PM"

Tarih - "g/aa/yyyy"

Yüzde - "0.00%"

Kesir - "# ?/?"

Bilimsel - "0.00E+00"

Muhasebe - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Renkle özel - "[Kırmızı]-#,##0.0"

## Örnekler

Grafik verilerinin biçim koduyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Balon grafiği ekleyin.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Veri etiketlerini göster.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Veri format kodlarını ayarlayın.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Ayrıca bakınız

* class [BubbleSizeCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
