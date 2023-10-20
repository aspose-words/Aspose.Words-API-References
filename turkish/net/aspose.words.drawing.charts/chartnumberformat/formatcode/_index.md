---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words for .NET
description: ChartNumberFormat FormatCode mülk. Bir veri etiketine uygulanan biçim kodunu alır veya ayarlar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

Bir veri etiketine uygulanan biçim kodunu alır veya ayarlar.

```csharp
public string FormatCode { get; set; }
```

## Notlar

Sayı biçimlendirmesi, bir değerin veri etiketinde görünme biçimini değiştirmek için kullanılır ve çok yaratıcı şekillerde kullanılabilir. Sayı biçimi örnekleri:

Sayı - "#,##0,00"

Para birimi - "\"$\"#,##0.00"

Saat - "[$-x-systime]sa:dd:ss AM/PM"

Tarih - "g/aa/yyyy"

Yüzde - "%0,00"

Kesir - "# ?/?"

Bilimsel - "0,00E+00"

Metin - "@"

Muhasebe - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_ -;_-@_-"

Renkle özel - "[Kırmızı]-#,##0.0"

## Örnekler

Grafik değerleri için biçimlendirmenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// Grafiğe X ekseni için kategoriler içeren özel bir seri ekleyin,
 // ve Y ekseni için ilgili büyük sayısal değerler.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Y ekseni onay etiketlerinin sayı biçimini, rakamları virgülle gruplandırmayacak şekilde ayarlayın.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Bu bayrak yukarıdaki değeri geçersiz kılabilir ve sayı biçimini kaynak hücreden çekebilir.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

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

* class [ChartNumberFormat](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
