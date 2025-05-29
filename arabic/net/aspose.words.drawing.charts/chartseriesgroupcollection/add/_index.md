---
title: ChartSeriesGroupCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ChartSeriesGroupCollection Add لإضافة مجموعات سلاسل جديدة بسهولة، مما يعزز قدرات تصور البيانات لديك.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing.charts/chartseriesgroupcollection/add/
---
## ChartSeriesGroupCollection.Add method

يضيف مجموعة سلسلة جديدة من نوع السلسلة المحدد إلى هذه المجموعة.

```csharp
public ChartSeriesGroup Add(ChartSeriesType seriesType)
```

## ملاحظات

يمكن أن تحتوي مخططات المجموعة على مجموعات سلاسل فقط من الأنواع التالية: المنطقة، والشريط، والعمود، والخط، والدائري، والمبعثر، والرادار، وأنواع الأسهم (باستثناء أنواع السلاسل ثلاثية الأبعاد المقابلة).

## أمثلة

يوضح كيفية العمل مع المحور الثانوي للرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

//حذف السلسلة المولدة افتراضيًا.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// قم بإنشاء مجموعة سلاسل إضافية، أيضًا من نوع الخط.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// حدد استخدام المحاور الثانوية لمجموعة السلسلة الجديدة.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
//إخفاء المحور X الثانوي.
newSeriesGroup.AxisX.Hidden = true;
// قم بتحديد عنوان المحور Y الثانوي.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

//أضف سلسلة إلى مجموعة السلسلة الجديدة.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### أنظر أيضا

* class [ChartSeriesGroup](../../chartseriesgroup/)
* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroupCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
