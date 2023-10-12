---
title: ChartYValue.FromDouble
second_title: Aspose.Words لمراجع .NET API
description: ChartYValue طريقة. إنشاء ملفChartYValue مثال علىDouble اكتب.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartyvalue/fromdouble/
---
## ChartYValue.FromDouble method

إنشاء ملف[`ChartYValue`](../) مثال علىDouble اكتب.

```csharp
public static ChartYValue FromDouble(double value)
```

### أمثلة

يوضح كيفية تعبئة سلسلة المخططات بالبيانات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// امسح قيم X وY من السلسلة الأولى.
series1.ClearValues();

// املأ السلسلة بالبيانات.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9), ChartYValue.FromDouble(17));

ChartSeries series2 = chart.Series[1];

// امسح قيم X وY للسلسلة الثانية.
series2.ClearValues();

// املأ السلسلة بالبيانات.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### أنظر أيضا

* class [ChartYValue](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartyvalue/)
* المجسم [Aspose.Words](../../../)


