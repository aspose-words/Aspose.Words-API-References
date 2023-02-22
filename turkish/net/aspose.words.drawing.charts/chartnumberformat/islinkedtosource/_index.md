---
title: ChartNumberFormat.IsLinkedToSource
second_title: Aspose.Words for .NET API Referansı
description: ChartNumberFormat mülk. Biçim kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. Varsayılan değer true.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

Biçim kodunun bir kaynak hücreye bağlı olup olmadığını belirtir. Varsayılan değer true.

```csharp
public bool IsLinkedToSource { get; set; }
```

### Notlar

Format kodu kaynağa bağlıysa NumberFormat genele sıfırlanacaktır.

### Örnekler

Grafik değerleri için biçimlendirmenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için kategorilerle grafiğe özel bir seri ekleyin,
 // ve Y ekseni için büyük ilgili sayısal değerler.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Y ekseni onay etiketlerinin sayı biçimini, basamakları virgülle gruplamayacak şekilde ayarlayın.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Bu bayrak, yukarıdaki değeri geçersiz kılabilir ve kaynak hücreden sayı biçimini çizebilir.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### Ayrıca bakınız

* class [ChartNumberFormat](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartnumberformat/)
* toplantı [Aspose.Words](../../../)


