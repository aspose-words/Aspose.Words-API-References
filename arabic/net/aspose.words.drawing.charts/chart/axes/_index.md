---
title: Chart.Axes
linktitle: Axes
articleTitle: Axes
second_title: Aspose.Words لـ .NET
description: Chart Axes ملكية. الحصول على مجموعة من جميع محاور هذا المخطط في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

الحصول على مجموعة من جميع محاور هذا المخطط.

```csharp
public ChartAxisCollection Axes { get; }
```

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

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
