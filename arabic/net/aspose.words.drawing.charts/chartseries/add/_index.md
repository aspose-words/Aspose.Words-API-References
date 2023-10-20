---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: ChartSeries Add طريقة. إضافة قيمة X المحددة إلى سلسلة المخططات. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات فستكون فارغة للقيمة X في C#.
type: docs
weight: 160
url: /ar/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

إضافة قيمة X المحددة إلى سلسلة المخططات. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة للقيمة X.

```csharp
public void Add(ChartXValue xValue)
```

### أنظر أيضا

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

إضافة قيم X وY المحددة إلى سلسلة المخططات.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
```

## أمثلة

يوضح كيفية إضافة/إزالة قيم بيانات المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// قم بإزالة القيمة الأولى في كلتا السلسلتين.
department1Series.Remove(0);
department2Series.Remove(0);

// أضف قيمًا جديدة إلى كلتا السلسلتين.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

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

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

إضافة قيمة X وقيمة Y وحجم الفقاعة المحددة إلى سلسلة المخطط.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

### أنظر أيضا

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
