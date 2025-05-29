---
title: ChartSeriesGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için toplam seri grubu sayısını ortaya çıkaran ChartSeriesGroupCollection'ın Count özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---
## ChartSeriesGroupCollection.Count property

Bu koleksiyondaki seri gruplarının sayısını döndürür.

```csharp
public int Count { get; }
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

* class [ChartSeriesGroupCollection](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
