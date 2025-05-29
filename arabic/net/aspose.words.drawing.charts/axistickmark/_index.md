---
title: AxisTickMark Enum
linktitle: AxisTickMark
articleTitle: AxisTickMark
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.Charts.AxisTickMark للحصول على مواضع علامات التجزئة القابلة للتخصيص، مما يعزز وضوح الرسم البياني وجاذبيته البصرية.
type: docs
weight: 850
url: /ar/net/aspose.words.drawing.charts/axistickmark/
---
## AxisTickMark enumeration

يحدد المواضع المحتملة لعلامات التجزئة.

```csharp
public enum AxisTickMark
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Cross | `0` | يحدد أن علامات التجزئة يجب أن تعبر المحور. |
| Inside | `1` | يحدد أن علامات التجزئة يجب أن تكون داخل منطقة الرسم البياني. |
| Outside | `2` | يحدد أن علامات التجزئة يجب أن تكون خارج منطقة الرسم البياني. |
| None | `3` | يحدد أنه لا ينبغي أن تكون هناك علامات اختيار. |

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
