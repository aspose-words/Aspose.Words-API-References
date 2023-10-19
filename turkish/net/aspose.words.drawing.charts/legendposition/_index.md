---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.LegendPosition Sıralama. Bir grafik açıklaması için olası konumları belirtir C#'da.
type: docs
weight: 910
url: /tr/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Bir grafik açıklaması için olası konumları belirtir.

```csharp
public enum LegendPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Grafikte herhangi bir açıklama gösterilmeyecek. |
| Bottom | `1` | Açıklamanın grafiğin alt kısmına çizileceğini belirtir. |
| Left | `2` | Açıklamanın grafiğin soluna çizileceğini belirtir. |
| Right | `3` | Açıklamanın grafiğin sağ tarafına çizileceğini belirtir. |
| Top | `4` | Açıklamanın grafiğin üst kısmına çizileceğini belirtir. |
| TopRight | `5` | Açıklamanın grafiğin sağ üst köşesine çizileceğini belirtir. |

## Örnekler

Bir grafiğin göstergesinin görünümünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Grafiğin açıklamasını sağ üst köşeye taşıyın.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Grafik gibi diğer grafik öğelerinin göstergeyle örtüşmesine izin vererek daha fazla alan verin.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
