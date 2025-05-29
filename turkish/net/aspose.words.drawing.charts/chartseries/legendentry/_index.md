---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: .NET için Aspose.Words
description: Grafikleriniz için gösterge girişlerine kolayca erişmek ve bunları özelleştirmek, böylece veri görselleştirmenizi geliştirmek için ChartSeries LegendEntry özelliğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Bu grafik serisi için bir gösterge girişi alır.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Örnekler

Efsane yazı tipiyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Tüm açıklama girişleri için varsayılan yazı tipi boyutunu ayarla.
chartLegend.Font.Size = 14;
// Belirli bir açıklama girişi için yazı tipini değiştir.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Grafik serileri için açıklama girişini al.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Ayrıca bakınız

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
