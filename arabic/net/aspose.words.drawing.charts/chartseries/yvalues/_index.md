---
title: ChartSeries.YValues
linktitle: YValues
articleTitle: YValues
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeries YValues للوصول إلى مجموعة قوية من قيم Y، مما يعزز قدراتك على تصور البيانات وتحليلها.
type: docs
weight: 150
url: /ar/net/aspose.words.drawing.charts/chartseries/yvalues/
---
## ChartSeries.YValues property

يحصل على مجموعة من قيم Y لسلسلة الرسم البياني هذه.

```csharp
public ChartYValueCollection YValues { get; }
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

* class [ChartYValueCollection](../../chartyvaluecollection/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
