---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: حسّن مخططاتك البيانية باستخدام طريقة ChartSeries Clear! احذف قيم البيانات وأعد ضبط التنسيق بسهولة للحصول على مظهر أنظف وأكثر احترافية.
type: docs
weight: 170
url: /ar/net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

يزيل جميع قيم البيانات من سلسلة المخططات. يُمسح تنسيق جميع نقاط البيانات الفردية وعلامات البيانات.

```csharp
public void Clear()
```

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

* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
