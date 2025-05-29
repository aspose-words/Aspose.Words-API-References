---
title: ChartXValueCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartXValueCollection FormatCode، وقم بتخصيص تنسيقات قيمة X بسهولة لتحسين تصور البيانات ووضوحها في مخططاتك.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartxvaluecollection/formatcode/
---
## ChartXValueCollection.FormatCode property

يحصل على رمز التنسيق المطبق على قيم X أو يعينه.

```csharp
public string FormatCode { get; set; }
```

## ملاحظات

يتم استخدام تنسيق الأرقام لتغيير طريقة ظهور القيم في الرسم البياني. أمثلة على تنسيقات الأرقام:

الرقم - "#,##0.00"

العملة - "\"$\"#,##0.00"

الوقت - "[$-x-systime]h:mm:ss AM/PM"

التاريخ - "د/ش/س"

النسبة المئوية - "0.00%"

جزء - "# ؟/؟"

علمي - "0.00E+00"

المحاسبة - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

مخصص باللون - "[أحمر]-#,##0.0"

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

* class [ChartXValueCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
