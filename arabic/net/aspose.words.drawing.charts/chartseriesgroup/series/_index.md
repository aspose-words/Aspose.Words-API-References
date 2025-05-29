---
title: ChartSeriesGroup.Series
linktitle: Series
articleTitle: Series
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeriesGroup Series للوصول إلى مجموعة فريدة من السلاسل ذات الصلة، مما يعزز تجربة تصور البيانات لديك.
type: docs
weight: 100
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/series/
---
## ChartSeriesGroup.Series property

يحصل على مجموعة من السلاسل التي تنتمي إلى مجموعة السلاسل هذه.

```csharp
public ChartSeriesCollection Series { get; }
```

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

* class [ChartSeriesCollection](../../chartseriescollection/)
* class [ChartSeriesGroup](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
