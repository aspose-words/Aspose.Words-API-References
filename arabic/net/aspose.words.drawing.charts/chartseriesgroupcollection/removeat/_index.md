---
title: ChartSeriesGroupCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words لـ .NET
description: احذف مجموعة سلاسل بسهولة باستخدام طريقة ChartSeriesGroupCollection RemoveAt. بسّط إدارة مخططاتك من خلال إزالة البيانات غير المرغوب فيها.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection.RemoveAt method

يزيل مجموعة سلاسل عند الفهرس المحدد. سيتم إزالة جميع السلاسل الفرعية من الرسم البياني.

```csharp
public void RemoveAt(int index)
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
