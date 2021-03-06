---
title: AxisBound
second_title: Aspose.Words لمراجع .NET API
description: يمثل الحد الأدنى أو الأقصى لقيم المحور.
type: docs
weight: 500
url: /ar/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

يمثل الحد الأدنى أو الأقصى لقيم المحور.

```csharp
public sealed class AxisBound
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [AxisBound](axisbound#constructor)() | إنشاء مثيل جديد يشير إلى أنه يجب تحديد حد المحور تلقائيًا بواسطة تطبيق معالجة الكلمات . |
| [AxisBound](axisbound#constructor_2)(DateTime) | يُنشئ محورًا منضمًا يتم تمثيله كقيمة للتاريخ والوقت. |
| [AxisBound](axisbound#constructor_1)(double) | لإنشاء حد محور يتم تمثيله كرقم . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto) { get; } | إرجاع إشارة تشير إلى أنه يجب تحديد حد المحور تلقائيًا. |
| [Value](../../aspose.words.drawing.charts/axisbound/value) { get; } | إرجاع القيمة الرقمية لحد المحور . |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate) { get; } | إرجاع قيمة منضم المحور ممثلة بالتاريخ والوقت. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals)(object) | لتحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode)() | يعمل كدالة تجزئة لهذا النوع. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring)() | إرجاع سلسلة سهلة الاستخدام تعرض قيمة هذا الكائن. |

### ملاحظات

يمكن تحديد الربط كقيمة رقمية أو تاريخ / وقت أو قيمة "تلقائية" خاصة.

حالات هذه الفئة غير قابلة للتغيير.

### أمثلة

يوضح كيفية إدراج مخطط بقيم التاريخ / الوقت.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// امسح سلسلة بيانات العرض التوضيحي للرسم البياني لتبدأ بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة تحتوي على قيم التاريخ / الوقت للمحور السيني ، والقيم العشرية ذات الصلة للمحور ص.
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

// قم بتعيين الوحدات الرئيسية للمحور X على أسبوع ، والوحدات الثانوية على يوم.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// تحديد خصائص المحور ص للقيم العشرية.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
