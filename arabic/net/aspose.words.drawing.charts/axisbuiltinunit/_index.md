---
title: AxisBuiltInUnit Enum
linktitle: AxisBuiltInUnit
articleTitle: AxisBuiltInUnit
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.Charts.AxisBuiltInUnit للحصول على وحدات عرض محور قابلة للتخصيص، مما يعزز وضوح الرسم البياني وفعاليته.
type: docs
weight: 760
url: /ar/net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

يحدد وحدات العرض للمحور.

```csharp
public enum AxisBuiltInUnit
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يحدد القيم الموجودة على الرسم البياني كما هي. |
| Custom | `1` | يُحدد أن القيم في الرسم البياني يجب قسمتها على قاسم مُحدد من قِبل المستخدم. هذه القيمة غير مدعومة من قِبل أنواع الرسوم البيانية الجديدة في MS Office 2016. |
| Billions | `2` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 1,000,000,000. |
| HundredMillions | `3` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 100,000,000. |
| Hundreds | `4` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 100. |
| HundredThousands | `5` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 100000. |
| Millions | `6` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 1,000,000. |
| TenMillions | `7` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 10,000,000. |
| TenThousands | `8` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 10000. |
| Thousands | `9` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 1000. |
| Trillions | `10` | يحدد القيم الموجودة على الرسم البياني التي سيتم تقسيمها على 1,000,000,000,0000. |
| Percentage | `11` | يُحدد أن القيم في الرسم البياني يجب قسمتها على 0.01. هذه القيمة مدعومة فقط من قِبل أنواع chart الجديدة في MS Office 2016. |

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
