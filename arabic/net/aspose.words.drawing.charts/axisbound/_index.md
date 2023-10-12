---
title: Class AxisBound
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.AxisBound فصل. يمثل الحد الأدنى أو الأقصى لقيم المحور.
type: docs
weight: 510
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
| [AxisBound](axisbound/#constructor)() | إنشاء مثيل جديد يشير إلى أنه يجب تحديد المحور المرتبط تلقائيًا بواسطة تطبيق معالجة الكلمات . |
| [AxisBound](axisbound/#constructor_2)(DateTime) | ينشئ محورًا محددًا يتم تمثيله كقيمة تاريخ ووقت. |
| [AxisBound](axisbound/#constructor_1)(double) | إنشاء محور محدد ممثلاً برقم. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | إرجاع علامة تشير إلى أنه يجب تحديد حدود المحور تلقائيًا. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | إرجاع القيمة الرقمية للمحور المرتبط. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | إرجاع قيمة المحور المحدود الممثل بالتاريخ والوقت. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(object) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | بمثابة وظيفة تجزئة لهذا النوع. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | تُرجع سلسلة سهلة الاستخدام تعرض قيمة هذا الكائن. |

### ملاحظات

يمكن تحديد المنضم كقيمة رقمية أو تاريخ أو قيمة "تلقائية" خاصة.

مثيلات هذه الفئة غير قابلة للتغيير.

### أمثلة

يوضح كيفية إدراج مخطط بقيم التاريخ/الوقت.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة تحتوي على قيم التاريخ/الوقت للمحور السيني، والقيم العشرية المعنية للمحور ص.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// تعيين الحدود الدنيا والعليا للمحور السيني.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// اضبط الوحدات الرئيسية للمحور السيني على أسبوع، والوحدات الصغيرة على يوم.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// تحديد خصائص المحور ص للقيم العشرية.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
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


