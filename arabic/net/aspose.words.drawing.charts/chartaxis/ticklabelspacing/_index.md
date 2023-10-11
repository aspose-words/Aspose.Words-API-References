---
title: ChartAxis.TickLabelSpacing
second_title: Aspose.Words لمراجع .NET API
description: ChartAxis ملكية. الحصول على أو تعيين الفاصل الزمني الذي يتم عنده رسم تسميات التجزئة.
type: docs
weight: 250
url: /ar/net/aspose.words.drawing.charts/chartaxis/ticklabelspacing/
---
## ChartAxis.TickLabelSpacing property

الحصول على أو تعيين الفاصل الزمني الذي يتم عنده رسم تسميات التجزئة.

```csharp
public int TickLabelSpacing { get; set; }
```

### ملاحظات

الخاصية لها تأثير على فئة النص ومحاور السلسلة. وهو غير مدعوم من قبل المخططات الجديدة لـ MS Office 2016 . النطاق الصالح للقيمة أكبر من أو يساوي 1.

يؤدي تعيين هذه الخاصية إلى تعيين[`TickLabelSpacingIsAuto`](../ticklabelspacingisauto/) الملكية ل`خطأ شنيع`.

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

* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartaxis/)
* المجسم [Aspose.Words](../../../)


