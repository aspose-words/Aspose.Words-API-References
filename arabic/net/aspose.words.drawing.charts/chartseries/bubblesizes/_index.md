---
title: ChartSeries.BubbleSizes
linktitle: BubbleSizes
articleTitle: BubbleSizes
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeries BubbleSizes للوصول إلى أحجام الفقاعات القابلة للتخصيص، مما يعزز تجربة تصور البيانات ورسم الرسوم البيانية الخاصة بك.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartseries/bubblesizes/
---
## ChartSeries.BubbleSizes property

يحصل على مجموعة من أحجام الفقاعات لسلسلة المخططات هذه.

```csharp
public BubbleSizeCollection BubbleSizes { get; }
```

## أمثلة

يوضح كيفية العمل مع كود تنسيق بيانات الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط فقاعي.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

//إظهار تسميات البيانات.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// تعيين رموز تنسيق البيانات.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### أنظر أيضا

* class [BubbleSizeCollection](../../bubblesizecollection/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
