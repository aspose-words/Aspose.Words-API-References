---
title: ChartXValue.FromString
linktitle: FromString
articleTitle: FromString
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ChartXValue FromString لإنشاء مثيلات ChartXValue من نوع String بسهولة. حسّن تصور بياناتك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue.FromString method

ينشئ[`ChartXValue`](../) مثال على ذلكString النوع.

```csharp
public static ChartXValue FromString(string value)
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

* class [ChartXValue](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
