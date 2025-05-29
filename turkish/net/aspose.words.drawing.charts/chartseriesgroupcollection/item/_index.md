---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Öğe özelliğiyle dizine göre ChartSeriesGroup'a erişin. Veri görselleştirmenizi basitleştirin ve grafik deneyiminizi zahmetsizce geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

Bir[`ChartSeriesGroup`](../../chartseriesgroup/) belirtilen dizinde.

```csharp
public ChartSeriesGroup this[int index] { get; }
```

## Örnekler

İkincil eksenin nasıl kaldırılacağını göster.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// İkincil ekseni bul ve koleksiyondan kaldır.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### Ayrıca bakınız

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
