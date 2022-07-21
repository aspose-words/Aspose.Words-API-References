---
title: AxisBound
second_title: Aspose.Words لمراجع .NET API
description: إنشاء مثيل جديد يشير إلى أنه يجب تحديد حد المحور تلقائيًا بواسطة تطبيق معالجة الكلمات .
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound() {#constructor}

إنشاء مثيل جديد يشير إلى أنه يجب تحديد حد المحور تلقائيًا بواسطة تطبيق معالجة الكلمات .

```csharp
public AxisBound()
```

### أمثلة

يوضح كيفية تعيين حدود المحور المخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// امسح سلسلة بيانات العرض التوضيحي للرسم البياني لتبدأ بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة ذات مصفوفتين عشريتين. تحتوي المصفوفة الأولى على قيم X ،
// والثاني يحتوي على قيم Y المقابلة للنقاط في المخطط المبعثر.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// بشكل افتراضي ، يتم تطبيق القياس الافتراضي على محوري الرسم البياني X و Y ،
// بحيث يكون كلا نطاقيهما كبيرًا بما يكفي ليشمل كل قيمة X و Y لكل سلسلة.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// يمكننا تحديد حدود المحور الخاصة بنا.
// في هذه الحالة ، سنجعل مساطر المحور X و Y تظهر نطاقًا من 0 إلى 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// إنشاء مخطط خطي بسلسلة تتطلب نطاقًا من التواريخ على المحور السيني والقيم العشرية للمحور ص.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// يمكننا أيضًا تعيين حدود المحور في شكل تواريخ أيضًا ، مع قصر الرسم البياني على فترة زمنية.
// سيؤدي تعيين النطاق إلى 1980-1990 إلى حذف قيمتي السلاسل
// التي تقع خارج النطاق من الرسم البياني.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### أنظر أيضا

* class [AxisBound](../../axisbound)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../axisbound)
* المجسم [Aspose.Words](../../../)

---

## AxisBound(double) {#constructor_1}

لإنشاء حد محور يتم تمثيله كرقم .

```csharp
public AxisBound(double value)
```

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

* class [AxisBound](../../axisbound)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../axisbound)
* المجسم [Aspose.Words](../../../)

---

## AxisBound(DateTime) {#constructor_2}

يُنشئ محورًا منضمًا يتم تمثيله كقيمة للتاريخ والوقت.

```csharp
public AxisBound(DateTime datetime)
```

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

* class [AxisBound](../../axisbound)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../axisbound)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
