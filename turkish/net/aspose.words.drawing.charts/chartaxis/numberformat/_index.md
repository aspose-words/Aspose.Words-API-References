---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için ChartNumberFormat nesnesini kullanarak grafiğinizin sayı biçimlerini zahmetsizce özelleştirmek üzere ChartAxis NumberFormat özelliğini keşfedin.
type: docs
weight: 200
url: /tr/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Bir[`ChartNumberFormat`](../../chartnumberformat/) eksen için sayı biçimlerinin tanımlanmasına izin veren nesne.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
