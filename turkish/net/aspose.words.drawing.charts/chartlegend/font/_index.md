---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: .NET için Aspose.Words
description: ChartLegend yazı tipi ayarlarınızı zahmetsizce özelleştirin! Varsayılan biçimlendirmeye erişin ve cilalı bir görünüm için belirli gösterge girişlerini kolayca geçersiz kılın.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

Efsane girişlerinin varsayılan yazı tipi biçimlendirmesine erişim sağlar. Belirli bir efsane girişi için yazı tipi biçimlendirmesini geçersiz kılmak için, kullanın[`Font`](../../chartlegendentry/font/) mülk.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegend](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
