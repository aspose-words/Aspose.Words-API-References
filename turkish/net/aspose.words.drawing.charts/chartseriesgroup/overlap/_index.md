---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için seri çubuklarınızın veya sütunlarınızın örtüşme yüzdesini kolayca ayarlamak üzere ChartSeriesGroup Örtüşme özelliğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Seri çubuklarının veya sütunlarının ne kadar örtüştüğünün yüzdesini alır veya ayarlar.

```csharp
public int Overlap { get; set; }
```

## Notlar

Tüm çubuk ve kolon tiplerinin seri gruplarına uygulanır.

Kabul edilebilir değerler aralığı -100 ile 100 dahil arasındadır. 0 değeri, çubuklar/sütunlar arasında boşluk olmadığını gösterir. Değer -100 ise, çubuklar/sütunlar arasındaki mesafe genişliklerine eşittir. 100 değeri, çubukların/sütunların tamamen örtüştüğü anlamına gelir.

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
