---
title: ChartSeriesGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Count في ChartSeriesGroupCollection، والتي تكشف عن العدد الإجمالي لمجموعات السلاسل لتحسين تصور البيانات.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---
## ChartSeriesGroupCollection.Count property

يعيد عدد مجموعات السلاسل في هذه المجموعة.

```csharp
public int Count { get; }
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

* class [ChartSeriesGroupCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
