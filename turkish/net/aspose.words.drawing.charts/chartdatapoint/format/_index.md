---
title: ChartDataPoint.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: ChartDataPoint Format mülk. Bu veri noktasının dolgu ve satır formatlamasına erişim sağlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Bu veri noktasının dolgu ve satır formatlamasına erişim sağlar.

```csharp
public ChartFormat Format { get; }
```

## Örnekler

Sütun grafiğinin kategorileri için ayrı ayrı biçimlendirmenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Varsayılan olarak oluşturulan seriyi silin.
chart.Series.Clear();

//Yeni seriler ekleniyor.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Sütun biçimlendirmesini ayarlayın.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

### Ayrıca bakınız

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
