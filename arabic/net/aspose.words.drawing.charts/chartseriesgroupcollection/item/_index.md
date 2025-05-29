---
title: ChartSeriesGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: الوصول إلى ChartSeriesGroup حسب الفهرس باستخدام خاصية العنصر. بسّط تصور بياناتك وحسّن تجربة إنشاء الرسوم البيانية بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartseriesgroupcollection/item/
---
## ChartSeriesGroupCollection indexer

يعيد[`ChartSeriesGroup`](../../chartseriesgroup/) عند الفهرس المحدد.

```csharp
public ChartSeriesGroup this[int index] { get; }
```

## أمثلة

إظهار كيفية إزالة المحور الثانوي.

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// ابحث عن المحور الثانوي وأزله من المجموعة.
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### أنظر أيضا

* class [ChartSeriesGroup](../../chartseriesgroup/)
* class [ChartSeriesGroupCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
