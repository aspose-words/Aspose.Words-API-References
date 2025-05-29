---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için grafik öğeleri arasındaki boşluk yüzdesini kolayca ayarlamak üzere ChartSeriesGroup GapWidth özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini alır veya ayarlar.

```csharp
public int GapWidth { get; set; }
```

## Notlar

Sadece çubuk, sütun, çubuk pastası, pasta pastası, histogram, kutu&amp;bıyık, şelale ve huni tiplerinin seri gruplarına uygulanır.

Kabul edilebilir değerler aralığı 0 ile 500 arasındadır. Çubuk/sütun tabanlı seri grupları için, the özelliği çubuk kümeleri arasındaki boşluğu genişliklerinin yüzdesi olarak temsil eder. Pasta-pasta ve pasta-çubuk grafikleri için bu, grafiğin birincil ve ikincil bölümleri arasındaki boşluktur.

## Örnekler

Boşluk genişliğinin ve örtüşmenin nasıl yapılandırılacağını gösterin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Sütun boşluk genişliğini ve örtüşmesini ayarlayın.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Ayrıca bakınız

* class [ChartSeriesGroup](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
