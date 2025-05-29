---
title: ChartAxis.BaseTimeUnit
linktitle: BaseTimeUnit
articleTitle: BaseTimeUnit
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BaseTimeUnit في ChartAxis لتحديد أصغر وحدة زمنية على محور فئة الوقت لديك بسهولة لتحسين تصور البيانات.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartaxis/basetimeunit/
---
## ChartAxis.BaseTimeUnit property

يقوم بإرجاع أو تعيين أصغر وحدة زمنية يتم تمثيلها على محور فئة الوقت.

```csharp
public AxisTimeUnit BaseTimeUnit { get; set; }
```

## ملاحظات

الخاصية لها تأثير فقط على محاور فئة الوقت.

## أمثلة

يوضح كيفية إدراج مخطط بقيم التاريخ/الوقت.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة تحتوي على قيم التاريخ/الوقت لمحور X، والقيم العشرية المقابلة لمحور Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// تعيين الحدود الدنيا والعليا لمحور X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// قم بتعيين الوحدات الرئيسية للمحور X إلى أسبوع، والوحدات الثانوية إلى يوم.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// قم بتحديد خصائص المحور Y للقيم العشرية.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### أنظر أيضا

* enum [AxisTimeUnit](../../axistimeunit/)
* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
