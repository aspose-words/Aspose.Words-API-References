---
title: Class AxisDisplayUnit
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.AxisDisplayUnit فصل. يوفر الوصول إلى خيارات القياس لوحدات العرض لمحور القيمة.
type: docs
weight: 550
url: /ar/net/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class

يوفر الوصول إلى خيارات القياس لوحدات العرض لمحور القيمة.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class AxisDisplayUnit
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [AxisDisplayUnit](axisdisplayunit/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomUnit](../../aspose.words.drawing.charts/axisdisplayunit/customunit/) { get; set; } | الحصول على مقسوم محدد من قبل المستخدم أو تعيينه لقياس وحدات العرض على محور القيمة. |
| [Document](../../aspose.words.drawing.charts/axisdisplayunit/document/) { get; } | إرجاع المستند الذي ينتمي إليه حامل العنوان. |
| [Unit](../../aspose.words.drawing.charts/axisdisplayunit/unit/) { get; set; } | الحصول على أو تعيين قيمة القياس لوحدات العرض كواحدة من القيم المحددة مسبقًا. |

### أمثلة

يوضح كيفية التعامل مع علامات التجزئة والقيم المعروضة لمحور المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// قم بتعيين علامات التجزئة الثانوية للمحور Y للإشارة بعيدًا عن منطقة الرسم،
// وعلامات التجزئة الرئيسية لعبور المحور.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// قم بتعيين المحور Y لإظهار علامة رئيسية كل 10 وحدات، وعلامة صغيرة كل وحدة واحدة.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// اضبط حدود المحور Y على -10 و20.
// سيعرض هذا المحور Y الآن 4 علامات تجزئة رئيسية و27 علامة تجزئة ثانوية.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// بالنسبة للمحور السيني، قم بتعيين علامات التجزئة الرئيسية عند كل 10 وحدات،
// كل علامة اختيار صغيرة عند 2.5 وحدة.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// قم بتكوين كلا النوعين من علامات التجزئة لتظهر داخل منطقة رسم الرسم البياني.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// قم بتعيين حدود المحور السيني بحيث يمتد المحور السيني إلى 5 علامات اختيار رئيسية و12 علامة اختيار ثانوية.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// قم بتعيين تسميات التجزئة لعرض قيمتها بالملايين.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// يمكننا تعيين قيمة أكثر تحديدًا ستعرض بها تسميات التجزئة قيمها.
// هذا البيان يعادل ما ورد أعلاه.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


