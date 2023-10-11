---
title: Chart.Axes
second_title: Aspose.Words لمراجع .NET API
description: Chart ملكية. الحصول على مجموعة من جميع محاور هذا المخطط.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

الحصول على مجموعة من جميع محاور هذا المخطط.

```csharp
public ChartAxisCollection Axes { get; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chart/)
* المجسم [Aspose.Words](../../../)


