---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.ChartAxisCollection فصل. يمثل مجموعة من محاور المخطط في C#.
type: docs
weight: 640
url: /ar/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

يمثل مجموعة من محاور المخطط.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | الحصول على عدد المحاور في هذه المجموعة. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | الحصول على المحور عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | يُرجع كائن العداد. |

## أمثلة

يوضح كيفية العمل مع مجموعة المحاور.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// إخفاء خطوط الشبكة الرئيسية على المحور Y الأساسي والثانوي.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### أنظر أيضا

* class [ChartAxis](../chartaxis/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
