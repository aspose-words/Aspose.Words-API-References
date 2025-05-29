---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: .NET için Aspose.Words
description: Grafik verimliliğinizi ve tutarlılığınızı artırmak için veri noktası biçimlerini endekse göre zahmetsizce çoğaltmak üzere ChartSeries CopyFormatFrom yöntemini keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

Belirtilen endekse sahip veri noktasından varsayılan veri noktası biçimini kopyalar.

```csharp
public void CopyFormatFrom(int dataPointIndex)
```

## Örnekler

Veri noktası biçiminin nasıl kopyalanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// Grafik ve seriyi güncel formata getir.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// 1 indeksli veri noktasının biçimini 2 indeksli veri noktasına kopyala
// böylece veri noktası 2, veri noktası 1 ile aynı görünür.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// 0 endeksli veri noktasının biçimini, tüm veri noktalarının varsayılan seri değerlerine kopyalayın.
// varsayılan formata sahip olan dizilerde veri noktası 0 ile aynı görünür.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### Ayrıca bakınız

* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
