---
title: ChartDataPoint.Format
linktitle: Format
articleTitle: Format
second_title: .NET için Aspose.Words
description: ChartDataPoint Format özelliğinin, etkili sunumlar için özelleştirilebilir dolgu ve çizgi stilleriyle veri görselleştirmenizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Bu veri noktasının dolgu ve satır biçimlendirmesine erişim sağlar.

```csharp
public ChartFormat Format { get; }
```

## Örnekler

Bir sütun grafiğinin kategorileri için ayrı ayrı biçimlendirmenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Varsayılan olarak oluşturulan seriyi sil.
chart.Series.Clear();

// Yeni seri ekleniyor.
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

Bir çizgi grafiğinde veri noktalarıyla nasıl çalışılacağını gösterir.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Grafiğin veri noktalarını elmas şekilleri şeklinde göstererek vurgulayın.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // İlk veri serisini temsil eden çizgiyi düzeltin.
    chart.Series[0].Smooth = true;

    // İlk serinin veri noktalarının, değer negatif olduğunda renklerinin tersine dönmeyeceğini doğrulayın.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Daha temiz görünümlü bir grafik için formatı tek tek temizleyebiliriz.
    dataPoint.ClearFormat();

    // Ayrıca bir dizi veri noktasını aynı anda soyabiliriz.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Bir diziye belirli sayıda veri noktası uygular.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### Ayrıca bakınız

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
