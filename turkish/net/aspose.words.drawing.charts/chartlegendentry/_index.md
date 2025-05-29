---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: .NET için Aspose.Words
description: Dinamik grafik efsaneleri oluşturmak için Aspose.Words.ChartLegendEntry sınıfını keşfedin. Sorunsuz entegrasyon ve özelleştirme ile veri görselleştirmenizi geliştirin.
type: docs
weight: 1020
url: /tr/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Bir grafik efsanesi girişini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartLegendEntry
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Bu efsane girişinin yazı tipi biçimlendirmesine erişim sağlar. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Bu girdinin grafik efsanesinde gizli olup olmadığını belirten bir değer alır veya ayarlar. Varsayılan değer**YANLIŞ** . |

## Notlar

Bir efsane girişi belirli bir grafik serisine veya trend çizgisine karşılık gelir.

Girişin metni, serinin veya trend çizgisinin adıdır. Metin değiştirilemez.

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

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
