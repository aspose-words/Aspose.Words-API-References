---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words لـ .NET
description: حسّن مخططاتك البيانية بسهولة باستخدام طريقة الإدراج ChartSeries. أدخل قيم X عند أي مؤشر، مما يُحسّن عرض بياناتك بسهولة!
type: docs
weight: 200
url: /ar/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

يُدرج قيمة X المحددة في سلسلة المخططات عند الفهرس المحدد. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة لقيمة X.

```csharp
public void Insert(int index, ChartXValue xValue)
```

## ملاحظات

سيتم إدراج نقطة البيانات المقابلة بتنسيق افتراضي في مجموعة نقاط البيانات. وإذا عُرضت تسميات البيانات، فسيتم إدراج تسمية البيانات المقابلة بتنسيق افتراضي أيضًا.

## أمثلة

يوضح كيفية إدراج البيانات في سلسلة مخططات بيانية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// مسح قيم X وY للسلسلة الأولى.
series1.ClearValues();
//ملء السلسلة بالبيانات.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### أنظر أيضا

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

يقوم بإدراج قيم X وY المحددة في سلسلة الرسم البياني عند الفهرس المحدد.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## ملاحظات

سيتم إدراج نقطة البيانات المقابلة بتنسيق افتراضي في مجموعة نقاط البيانات. وإذا عُرضت تسميات البيانات، فسيتم إدراج تسمية البيانات المقابلة بتنسيق افتراضي أيضًا.

## أمثلة

يوضح كيفية إدراج البيانات في سلسلة مخططات بيانية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// مسح قيم X وY للسلسلة الأولى.
series1.ClearValues();
//ملء السلسلة بالبيانات.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### أنظر أيضا

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

يقوم بإدراج قيمة X وقيمة Y وحجم الفقاعة المحددة في سلسلة الرسم البياني عند الفهرس المحدد.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## ملاحظات

سيتم إدراج نقطة البيانات المقابلة بتنسيق افتراضي في مجموعة نقاط البيانات. وإذا عُرضت تسميات البيانات، فسيتم إدراج تسمية البيانات المقابلة بتنسيق افتراضي أيضًا.

## أمثلة

يوضح كيفية إدراج البيانات في سلسلة مخططات بيانية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// مسح قيم X وY للسلسلة الأولى.
series1.ClearValues();
//ملء السلسلة بالبيانات.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### أنظر أيضا

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
