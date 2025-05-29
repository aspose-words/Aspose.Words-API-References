---
title: AxisDisplayUnit.CustomUnit
linktitle: CustomUnit
articleTitle: CustomUnit
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CustomUnit في AxisDisplayUnit لتخصيص وحدات عرض محور القيمة بسهولة باستخدام مقياس محدد من قبل المستخدم لتحسين وضوح البيانات.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/axisdisplayunit/customunit/
---
## AxisDisplayUnit.CustomUnit property

يحصل على أو يعين قاسمًا محددًا من قبل المستخدم لقياس وحدات العرض على محور القيمة.

```csharp
public double CustomUnit { get; set; }
```

## ملاحظات

لا تدعم مخططات MS Office 2016 الجديدة هذه الخاصية. القيمة الافتراضية هي 1.

يؤدي تعيين هذه الخاصية إلى تعيين[`Unit`](../unit/) الخاصية to Custom.

## أمثلة

يوضح كيفية التعامل مع علامات التجزئة والقيم المعروضة على محور الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// قم بتعيين علامات التجزئة الثانوية للمحور Y بحيث تشير بعيدًا عن منطقة الرسم البياني،
// وعلامات التجزئة الرئيسية لعبور المحور.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// قم بضبط المحور Y لإظهار علامة رئيسية كل 10 وحدات، وعلامة ثانوية كل وحدة واحدة.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// تعيين حدود المحور Y إلى -10 و20.
// سيعرض المحور Y الآن 4 علامات رئيسية و27 علامة ثانوية.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// بالنسبة للمحور X، اضبط علامات التجزئة الرئيسية عند كل 10 وحدات،
// كل علامة صغيرة عند 2.5 وحدة.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// قم بتكوين كلا النوعين من علامات الاختيار لتظهر داخل منطقة رسم الرسم البياني.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// قم بتعيين حدود المحور X بحيث يمتد المحور X على 5 علامات رئيسية و12 علامة ثانوية.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// قم بتعيين علامات التجزئة لعرض قيمتها بالملايين.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// يمكننا تعيين قيمة أكثر تحديدًا لعرض قيم علامات التجزئة.
//هذا البيان يعادل البيان أعلاه.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### أنظر أيضا

* class [AxisDisplayUnit](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
