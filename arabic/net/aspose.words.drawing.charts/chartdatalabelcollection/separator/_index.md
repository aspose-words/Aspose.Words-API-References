---
title: ChartDataLabelCollection.Separator
linktitle: Separator
articleTitle: Separator
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الفاصل في ChartDataLabelCollection. خصّص فواصل تسميات البيانات لتحسين وضوح مخططاتك، بدءًا من الفواصل وصولًا إلى فواصل الأسطر.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

يحصل على أو يعين فاصل السلسلة المستخدم لعلامات البيانات الخاصة بالسلسلة بأكملها. الافتراضي هو فاصلة، باستثناء المخططات الدائرية التي تعرض اسم الفئة والنسبة المئوية فقط، عندما يتم استخدام فاصل الأسطر بدلاً من ذلك.

```csharp
public string Separator { get; set; }
```

## ملاحظات

يمكن تجاوز القيمة المحددة لهذه الخاصية لعلامة بيانات فردية باستخدام [`Separator`](../../chartdatalabel/separator/) الملكية.

## أمثلة

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

 // أضف سلسلة مخصصة مع إحداثيات X/Y وقطر كل فقاعة.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// تمكين تسميات البيانات، ثم تعديل مظهرها.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// قم بإدراج سلسلة مخططات مخصصة مع اسم الفئة لكل قطاع، وجدول التردد الخاص بها.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// تمكين تسميات البيانات التي ستعرض النسبة المئوية والتردد لكل قطاع، وتعديل مظهرها.
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
