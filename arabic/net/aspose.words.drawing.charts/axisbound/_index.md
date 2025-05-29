---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.AxisBound، الحل الخاص بك لتحديد حدود قيمة المحور في المخططات لتصور البيانات بدقة.
type: docs
weight: 750
url: /ar/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

يمثل الحد الأدنى أو الأقصى لقيم المحور.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public sealed class AxisBound
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | ينشئ مثيلًا جديدًا يشير إلى أنه يجب تحديد حدود المحور تلقائيًا بواسطة تطبيق معالجة الكلمات . |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | ينشئ حدودًا للمحور يتم تمثيلها كقيمة تاريخ ووقت. |
| [AxisBound](axisbound/#constructor_1)(*double*) | ينشئ حدود المحور التي يتم تمثيلها كرقم. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | يعيد علمًا يشير إلى أنه يجب تحديد حدود المحور تلقائيًا. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | يعيد القيمة العددية لحدود المحور. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | يعيد قيمة حدود المحور الممثلة بالتاريخ والوقت. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | يعمل كدالة تجزئة لهذا النوع. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | يعيد سلسلة سهلة الاستخدام تعرض قيمة هذا الكائن. |

## ملاحظات

يمكن تحديد الحد كقيمة رقمية أو تاريخ ووقت أو قيمة "تلقائية" خاصة.

إن حالات هذه الفئة غير قابلة للتغيير.

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
