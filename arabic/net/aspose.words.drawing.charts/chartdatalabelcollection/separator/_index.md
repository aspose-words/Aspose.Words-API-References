---
title: ChartDataLabelCollection.Separator
linktitle: Separator
articleTitle: Separator
second_title: Aspose.Words لـ .NET
description: ChartDataLabelCollection Separator ملكية. الحصول على أو تعيين فاصل السلسلة المستخدم لتسميات البيانات الخاصة بالسلسلة بأكملها. الإعداد الافتراضي هو فاصلة باستثناء المخططات الدائرية التي تعرض اسم الفئة والنسبة المئوية فقط عند استخدام فاصل الأسطر بدلاً من ذلك في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

الحصول على أو تعيين فاصل السلسلة المستخدم لتسميات البيانات الخاصة بالسلسلة بأكملها. الإعداد الافتراضي هو فاصلة، باستثناء المخططات الدائرية التي تعرض اسم الفئة والنسبة المئوية فقط، عند استخدام فاصل الأسطر بدلاً من ذلك.

```csharp
public string Separator { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لتسمية بيانات فردية باستخدام [`Separator`](../../chartdatalabel/separator/) الملكية.

## أمثلة

يوضح كيفية التعامل مع تسميات البيانات الخاصة بالمخطط الفقاعي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة بإحداثيات X/Y وقطر كل من الفقاعات.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// قم بتمكين تسميات البيانات، ثم قم بتعديل مظهرها.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

يوضح كيفية التعامل مع تسميات البيانات الخاصة بالمخطط الدائري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أدخل سلسلة مخططات مخصصة مع اسم فئة لكل قطاع وجدول تكرارها.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// تمكين تسميات البيانات التي ستعرض النسبة المئوية والتكرار لكل قطاع، وتعديل مظهرها.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### أنظر أيضا

* class [ChartDataLabelCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
