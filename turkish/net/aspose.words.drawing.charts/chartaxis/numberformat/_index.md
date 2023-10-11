---
title: ChartAxis.NumberFormat
second_title: Aspose.Words for .NET API Referansı
description: ChartAxis mülk. Bir değeri döndürürChartNumberFormat eksen için sayı formatlarının tanımlanmasına izin veren nesne.
type: docs
weight: 190
url: /tr/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

Bir değeri döndürür[`ChartNumberFormat`](../../chartnumberformat/) eksen için sayı formatlarının tanımlanmasına izin veren nesne.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### Örnekler

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartaxis/)
* toplantı [Aspose.Words](../../../)


