---
title: Chart.Axes
linktitle: Axes
articleTitle: Axes
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "محاور المخطط" للوصول إلى جميع محاور المخطط بسهولة. حسّن تصور بياناتك من خلال إدارة شاملة للمحاور.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

يحصل على مجموعة من جميع محاور هذا الرسم البياني.

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

// إخفاء خطوط الشبكة الرئيسية على المحورين Y الأساسي والثانوي.
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
