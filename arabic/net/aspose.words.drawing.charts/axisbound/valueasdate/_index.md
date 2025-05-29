---
title: AxisBound.ValueAsDate
linktitle: ValueAsDate
articleTitle: ValueAsDate
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية AxisBound ValueAsDate، التي تقوم بإرجاع القيم المرتبطة بالمحور بكفاءة كتاريخ ووقت لتحسين تصور البيانات وتحليلها.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/axisbound/valueasdate/
---
## AxisBound.ValueAsDate property

يعيد قيمة حدود المحور الممثلة بالتاريخ والوقت.

```csharp
public DateTime ValueAsDate { get; }
```

## أمثلة

يوضح كيفية تعيين حدود المحور المخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// أضف سلسلة من مصفوفتين عشريتين. تحتوي المصفوفة الأولى على قيم X،
// والثاني يحتوي على قيم Y المقابلة للنقاط في مخطط التشتت.
chart.Series.Add("Series 1",
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 },
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// بشكل افتراضي، يتم تطبيق التدرج الافتراضي على المحورين X وY للرسم البياني،
// بحيث يكون كلا النطاقين كبيرين بما يكفي لاحتواء كل قيمة X و Y لكل سلسلة.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

//يمكننا تحديد حدود المحور الخاصة بنا.
// في هذه الحالة، سنجعل مسطرتي المحور X والمحور Y تظهران نطاقًا يتراوح بين 0 إلى 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// قم بإنشاء مخطط خطي بسلسلة تتطلب نطاقًا من التواريخ على المحور X، وقيمًا عشرية على المحور Y.
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

// يمكننا أيضًا تعيين حدود المحور في شكل تواريخ، مما يحد من الرسم البياني إلى فترة زمنية.
// سيؤدي تعيين النطاق إلى 1980-1990 إلى حذف القيمتين المتسلسلتين
//التي تقع خارج النطاق من الرسم البياني.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### أنظر أيضا

* class [AxisBound](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
