---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartNumberFormat sınıf. Ana öğenin sayı biçimlendirmesini temsil eder C#'da.
type: docs
weight: 770
url: /tr/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

Ana öğenin sayı biçimlendirmesini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartNumberFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | Bir veri etiketine uygulanan biçim kodunu alır veya ayarlar. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | Biçim kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. Varsayılan doğrudur. |

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
