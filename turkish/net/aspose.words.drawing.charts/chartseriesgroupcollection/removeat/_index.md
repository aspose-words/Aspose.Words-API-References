---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: .NET için Aspose.Words
description: ChartSeriesGroupCollection RemoveAt yöntemi ile bir seri grubunu zahmetsizce kaldırın. İstenmeyen verileri ortadan kaldırarak grafik yönetiminizi basitleştirin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

Belirtilen dizindeki bir seri grubunu kaldırır. Tüm alt seriler grafikten kaldırılır.

```csharp
public void RemoveAt(int index)
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
