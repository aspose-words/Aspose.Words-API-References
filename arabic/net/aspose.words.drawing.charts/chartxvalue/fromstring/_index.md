---
title: ChartXValue.FromString
second_title: Aspose.Words لمراجع .NET API
description: ChartXValue طريقة. إنشاء ملفChartXValue مثال علىString اكتب.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

إنشاء ملف[`ChartXValue`](../) مثال علىString اكتب.

```csharp
public static ChartXValue FromString(string value)
```

### أمثلة

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

### أنظر أيضا

* class [ChartXValue](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartxvalue/)
* المجسم [Aspose.Words](../../../)


