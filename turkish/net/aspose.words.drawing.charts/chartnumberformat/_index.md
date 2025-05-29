---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: .NET için Aspose.Words
description: Grafiklerde gelişmiş sayı biçimlendirmesi için Aspose.Words.Drawing.Charts.ChartNumberFormat sınıfını keşfedin. Belgenizin görsel çekiciliğini artırın!
type: docs
weight: 1060
url: /tr/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

Üst öğenin sayı biçimlendirmesini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartNumberFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | Bir veri etiketine uygulanan biçim kodunu alır veya ayarlar. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | Biçim kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. Varsayılan değer doğrudur. |

## Örnekler

Grafik değerleri için biçimlendirmenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için kategorilerle grafiğe özel bir seri ekleyin,
 // ve Y ekseni için büyük sayısal değerler.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Y eksenindeki işaret etiketlerinin sayı biçimini, basamakların virgüllerle gruplanmaması için ayarlayın.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Bu bayrak yukarıdaki değeri geçersiz kılabilir ve sayı biçimini kaynak hücreden çizebilir.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
