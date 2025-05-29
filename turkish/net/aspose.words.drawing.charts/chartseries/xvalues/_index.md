---
title: ChartSeries.XValues
linktitle: XValues
articleTitle: XValues
second_title: .NET için Aspose.Words
description: Güçlü bir X değerleri koleksiyonuna erişmek ve veri görselleştirmenizi ve analizinizi geliştirmek için ChartSeries XValues özelliğini keşfedin.
type: docs
weight: 140
url: /tr/net/aspose.words.drawing.charts/chartseries/xvalues/
---
## ChartSeries.XValues property

Bu grafik serisi için X değerlerinin bir koleksiyonunu alır.

```csharp
public ChartXValueCollection XValues { get; }
```

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

* class [ChartXValueCollection](../../chartxvaluecollection/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
