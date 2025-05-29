---
title: ChartSeries.XValues
linktitle: XValues
articleTitle: XValues
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeries XValues للوصول إلى مجموعة قوية من قيم X، مما يعزز تصور البيانات وتحليلها.
type: docs
weight: 140
url: /ar/net/aspose.words.drawing.charts/chartseries/xvalues/
---
## ChartSeries.XValues property

يحصل على مجموعة من قيم X لسلسلة الرسم البياني هذه.

```csharp
public ChartXValueCollection XValues { get; }
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

* class [ChartXValueCollection](../../chartxvaluecollection/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
