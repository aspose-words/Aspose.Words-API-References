---
title: ChartLegendEntryCollection Class
linktitle: ChartLegendEntryCollection
articleTitle: ChartLegendEntryCollection
second_title: .NET için Aspose.Words
description: Grafik açıklama girişlerini etkili bir şekilde yönetmek ve belge görsellerinizi kolaylıkla geliştirmek için Aspose.Words.ChartLegendEntryCollection'ı keşfedin.
type: docs
weight: 1030
url: /tr/net/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class

Grafik efsanesi girişlerinin bir koleksiyonunu temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartLegendEntryCollection : IEnumerable<ChartLegendEntry>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartlegendentrycollection/count/) { get; } | sayısını döndürür[`ChartLegendEntry`](../chartlegendentry/) bu koleksiyonda. |
| [Item](../../aspose.words.drawing.charts/chartlegendentrycollection/item/) { get; } | Geri Döndürür[`ChartLegendEntry`](../chartlegendentry/) belirtilen dizin için. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartlegendentrycollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |

## Örnekler

Grafik serileri için bir gösterge girişiyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Ayrıca bakınız

* class [ChartLegendEntry](../chartlegendentry/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
