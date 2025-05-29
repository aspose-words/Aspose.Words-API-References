---
title: ChartSeries.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words لـ .NET
description: احذف قيم X وY وأحجام الفقاعات من سلسلة مخططاتك بسهولة باستخدام طريقة إزالة ChartSeries. بسّط عملية تصور بياناتك اليوم!
type: docs
weight: 210
url: /ar/net/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries.Remove method

يزيل قيمة X وقيمة Y وحجم الفقاعة، إذا كان مدعومًا، من سلسلة الرسم البياني عند الفهرس المحدد. تتم أيضًا إزالة نقطة البيانات المقابلة وعلامة البيانات.

```csharp
public void Remove(int index)
```

## أمثلة

يوضح كيفية إضافة/إزالة قيم بيانات الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// قم بإزالة القيمة الأولى في كلا السلسلتين.
department1Series.Remove(0);
department2Series.Remove(0);

//أضف قيمًا جديدة إلى كلتا السلسلتين.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

### أنظر أيضا

* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
