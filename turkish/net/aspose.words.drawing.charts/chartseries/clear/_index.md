---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: .NET için Aspose.Words
description: ChartSeries Clear yöntemi ile grafiklerinizi optimize edin! Daha temiz, daha profesyonel bir görünüm için veri değerlerini zahmetsizce kaldırın ve biçimlendirmeyi sıfırlayın.
type: docs
weight: 170
url: /tr/net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

Grafik serisinden tüm veri değerlerini kaldırır. Tüm bireysel veri noktalarının ve veri etiketlerinin biçimi temizlenir.

```csharp
public void Clear()
```

## Örnekler

Grafik serilerinin verilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// İlk serinin X ve Y değerlerini temizle.
series1.ClearValues();

// Seriyi verilerle doldur.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// İkinci serinin X ve Y değerlerini temizle.
series2.Clear();

// Seriyi verilerle doldur.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Ayrıca bakınız

* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
