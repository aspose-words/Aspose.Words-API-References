---
title: Enum AxisBuiltInUnit
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.AxisBuiltInUnit تعداد. تحديد وحدات العرض للمحور.
type: docs
weight: 520
url: /ar/net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

تحديد وحدات العرض للمحور.

```csharp
public enum AxisBuiltInUnit
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يحدد القيم الموجودة على المخطط والتي سيتم عرضها كما هي. |
| Custom | `1` | يحدد أن القيم الموجودة على المخطط يجب أن يتم تقسيمها بواسطة المقسوم عليه بواسطة المستخدم. هذه القيمة غير مدعومة بواسطة أنواع المخططات الجديدة لـ MS Office 2016. |
| Billions | `2` | تحديد القيم الموجودة على المخطط والتي يجب تقسيمها على 1,000,000,000. |
| HundredMillions | `3` | تحديد القيم الموجودة على المخطط والتي يجب تقسيمها على 100,000,000. |
| Hundreds | `4` | يحدد تقسيم القيم على المخطط على 100. |
| HundredThousands | `5` | تحديد القيم الموجودة على المخطط والتي يجب تقسيمها على 100,000. |
| Millions | `6` | تحديد القيم الموجودة على المخطط والتي يجب تقسيمها على 1,000,000. |
| TenMillions | `7` | تحديد القيم الموجودة على المخطط والتي يجب تقسيمها على 10,000,000. |
| TenThousands | `8` | تحديد القيم الموجودة على المخطط والتي يجب تقسيمها على 10,000. |
| Thousands | `9` | تحديد القيم الموجودة على المخطط والتي يجب تقسيمها على 1,000. |
| Trillions | `10` | تحديد القيم الموجودة على المخطط والتي سيتم تقسيمها على 1,000,000,000,0000. |
| Percentage | `11` | يحدد القيم الموجودة على المخطط والتي يجب تقسيمها على 0.01. يتم دعم هذه القيمة فقط من خلال أنواع Chart الجديدة من MS Office 2016. |

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


