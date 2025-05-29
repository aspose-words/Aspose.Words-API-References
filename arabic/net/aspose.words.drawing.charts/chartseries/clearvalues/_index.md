---
title: ChartSeries.ClearValues
linktitle: ClearValues
articleTitle: ClearValues
second_title: Aspose.Words لـ .NET
description: اكتشف ChartSeries ClearValues. احذف قيم البيانات بسهولة مع الحفاظ على تنسيق مخططك وتسمياته لمظهر أكثر أناقة واحترافية.
type: docs
weight: 180
url: /ar/net/aspose.words.drawing.charts/chartseries/clearvalues/
---
## ChartSeries.ClearValues method

يزيل جميع قيم البيانات من سلسلة الرسم البياني مع الحفاظ على تنسيق نقاط البيانات وعلامات البيانات.

```csharp
public void ClearValues()
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
