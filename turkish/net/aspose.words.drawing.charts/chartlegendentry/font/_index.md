---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: .NET için Aspose.Words
description: Özelleştirilebilir yazı tipi biçimlendirmesine kolay erişim için ChartLegendEntry Font özelliğini keşfedin ve daha iyi görsel çekicilik için açıklama girişlerinizi geliştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Bu efsane girişinin yazı tipi biçimlendirmesine erişim sağlar.

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
* class [ChartLegendEntry](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
