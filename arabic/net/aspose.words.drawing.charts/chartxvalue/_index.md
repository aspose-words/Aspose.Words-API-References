---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartXValue، الحل الخاص بك لتحديد قيم X في سلسلة المخططات، مما يعزز تصور البيانات بسهولة.
type: docs
weight: 1160
url: /ar/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

يمثل قيمة X لسلسلة الرسم البياني.

```csharp
public class ChartXValue
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | يحصل على قيمة التاريخ والوقت المخزنة. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | يحصل على القيمة الرقمية المخزنة. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | يحصل على القيمة المخزنة متعددة المستويات. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | يحصل على قيمة السلسلة المخزنة. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | يحصل على قيمة الوقت المخزنة. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | يحصل على نوع قيمة X المخزنة في الكائن. |

## طُرق

| اسم | وصف |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | ينشئ`ChartXValue` مثال على ذلكDateTime النوع. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | ينشئ`ChartXValue` مثال على ذلكDouble النوع. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | ينشئ`ChartXValue` مثال على ذلكMultilevel النوع. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | ينشئ`ChartXValue` مثال على ذلكString النوع. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | ينشئ`ChartXValue` مثال على ذلكTime النوع. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | يحصل على علم يشير إلى ما إذا كان الكائن المحدد يساوي قيمة الكائن X الحالية. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | يحصل على رمز تجزئة لكائن القيمة X الحالي. |

## ملاحظات

تحتوي هذه الفئة على عدد من الطرق الثابتة لإنشاء قيمة X من نوع معين. The [`ValueType`](./valuetype/) تتيح لك الخاصية تحديد نوع قيمة X الموجودة.

يجب أن تكون جميع قيم X غير الصفرية لسلسلة الرسم البياني من نفس القيمة[`ChartXValueType`](../chartxvaluetype/) يكتب.

## أمثلة

يوضح كيفية ملء سلسلة المخططات بالبيانات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// مسح قيم X وY للسلسلة الأولى.
series1.ClearValues();

//ملء السلسلة بالبيانات.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// مسح قيم X و Y للسلسلة الثانية.
series2.Clear();

//ملء السلسلة بالبيانات.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
