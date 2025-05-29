---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.ChartSeriesGroupCollection، الحل الأمثل لإدارة وتنظيم كائنات ChartSeriesGroup بسهولة.
type: docs
weight: 1100
url: /ar/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

يمثل مجموعة من[`ChartSeriesGroup`](../chartseriesgroup/) الأشياء.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | يعيد عدد مجموعات السلاسل في هذه المجموعة. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | يعيد[`ChartSeriesGroup`](../chartseriesgroup/) عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | يضيف مجموعة سلسلة جديدة من نوع السلسلة المحدد إلى هذه المجموعة. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | يعيد كائن المعداد. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | يزيل مجموعة سلاسل عند الفهرس المحدد. سيتم إزالة جميع السلاسل الفرعية من الرسم البياني. |

## ملاحظات

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية .

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
