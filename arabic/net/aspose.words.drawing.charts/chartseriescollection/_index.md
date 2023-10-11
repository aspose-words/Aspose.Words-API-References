---
title: Class ChartSeriesCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartSeriesCollection فصل. يمثل مجموعة منChartSeries .
type: docs
weight: 790
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
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | إرجاع أ[`ChartSeries`](../chartseries/) في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(string, DateTime[], double[]) | يضيف الجديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات المساحية والرادارية والأسهم. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(string, double[], double[]) | يضيف الجديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات المبعثرة. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(string, string[], double[]) | يضيف الجديد[`ChartSeries`](../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات الشريطية والعمودية والخطية والسطحية. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(string, double[], double[], double[]) | يضيف الجديد[`ChartSeries`](../chartseries/)إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات الفقاعية. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | يزيل الكل[`ChartSeries`](../chartseries/) من هذه المجموعة. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | يُرجع كائن العداد. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(int) | يزيل أ[`ChartSeries`](../chartseries/) في الفهرس المحدد. |

### أمثلة

يوضح كيفية إضافة وإزالة بيانات السلسلة في مخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مخططًا عموديًا يحتوي على ثلاث سلاسل من البيانات التوضيحية افتراضيًا.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// تحتوي كل سلسلة على أربع قيم عشرية: واحدة لكل فئة من الفئات الأربع.
// أربع مجموعات من ثلاثة أعمدة ستمثل هذه البيانات.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// اطبع اسم كل سلسلة في المخطط.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// هذه هي أسماء الفئات الموجودة في المخطط.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// يمكننا إضافة سلسلة بقيم جديدة للفئات الموجودة.
// سيحتوي هذا المخطط الآن على أربع مجموعات من أربعة أعمدة.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// يمكن أيضًا إزالة سلسلة المخططات عن طريق الفهرس، مثل هذا.
// سيؤدي هذا إلى إزالة إحدى السلاسل التجريبية الثلاثة المرفقة مع المخطط.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// يمكننا أيضًا مسح جميع بيانات المخطط مرة واحدة باستخدام هذه الطريقة.
// عند إنشاء مخطط جديد، هذه هي الطريقة لمسح كافة البيانات التجريبية
// قبل أن نبدأ العمل على مخطط فارغ.
chartData.Clear();
```

### أنظر أيضا

* class [ChartSeries](../chartseries/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


