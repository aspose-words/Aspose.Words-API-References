---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartSeriesCollection، الحل الخاص بك لإدارة سلسلة المخططات وتخصيصها بسهولة.
type: docs
weight: 1080
url: /ar/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

يمثل مجموعة من[`ChartSeries`](../chartseries/) .

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | إرجاع عدد[`ChartSeries`](../chartseries/) في هذه المجموعة. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | يعيد[`ChartSeries`](../chartseries/) عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[]*) | يضيف جديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى مخططات الهيستوغرام. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, ChartMultilevelValue[], double[]*) | يضيف جديد[`ChartSeries`](../chartseries/)إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة تحتوي على فئات بيانات متعددة المستويات. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_4)(*string, DateTime[], double[]*) | يضيف جديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات المساحية والرادارية والأسهم. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, double[], double[]*) | يضيف جديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من مخططات التشتت. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_5)(*string, string[], double[]*) | يضيف جديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات الشريطية والعمودية والخطية والسطحية. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, double[], double[], double[]*) | يضيف جديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من مخططات الفقاعات. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_6)(*string, string[], double[], bool[]*) | يضيف جديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى مخططات الشلال. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | يزيل الكل[`ChartSeries`](../chartseries/) من هذه المجموعة. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | يعيد كائن المعداد. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | يزيل[`ChartSeries`](../chartseries/) عند الفهرس المحدد. |

## أمثلة

يوضح كيفية إضافة بيانات السلسلة وإزالتها في مخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج مخطط عمودي يحتوي على ثلاث سلاسل من البيانات التجريبية بشكل افتراضي.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// تحتوي كل سلسلة على أربع قيم عشرية: واحدة لكل فئة من الفئات الأربع.
//ستمثل أربع مجموعات من ثلاثة أعمدة هذه البيانات.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// اطبع اسم كل سلسلة في الرسم البياني.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

//هذه هي أسماء الفئات الموجودة في الرسم البياني.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

//يمكننا إضافة سلسلة بقيم جديدة للفئات الموجودة.
// سيحتوي هذا الرسم البياني الآن على أربع مجموعات مكونة من أربعة أعمدة.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
//يمكن أيضًا إزالة سلسلة الرسم البياني بواسطة الفهرس، مثل هذا.
// سيؤدي هذا إلى إزالة إحدى سلاسل العروض التوضيحية الثلاثة التي جاءت مع الرسم البياني.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
//يمكننا أيضًا مسح جميع بيانات الرسم البياني مرة واحدة باستخدام هذه الطريقة.
// عند إنشاء مخطط جديد، هذه هي الطريقة لمسح جميع بيانات العرض التوضيحي
// قبل أن نتمكن من البدء في العمل على مخطط فارغ.
chartData.Clear();
```

### أنظر أيضا

* class [ChartSeries](../chartseries/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
