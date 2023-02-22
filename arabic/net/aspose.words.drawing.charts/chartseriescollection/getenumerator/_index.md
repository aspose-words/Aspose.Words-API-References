---
title: ChartSeriesCollection.GetEnumerator
second_title: Aspose.Words لمراجع .NET API
description: ChartSeriesCollection طريقة. إرجاع كائن العداد .
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartseriescollection/getenumerator/
---
## ChartSeriesCollection.GetEnumerator method

إرجاع كائن العداد .

```csharp
public IEnumerator<ChartSeries> GetEnumerator()
```

### أمثلة

يوضح كيفية إضافة وإزالة بيانات السلاسل في مخطط.

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

// هذه هي أسماء الفئات في الرسم البياني.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// يمكننا إضافة سلسلة بقيم جديدة للفئات الموجودة.
// سيحتوي هذا المخطط الآن على أربع مجموعات من أربعة أعمدة.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });

// يمكن أيضًا إزالة سلسلة المخططات بالفهرس ، مثل هذا.
// سيؤدي ذلك إلى إزالة إحدى السلاسل التجريبية الثلاثة المرفقة مع الرسم البياني.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));

// يمكننا أيضًا مسح جميع بيانات الرسم البياني مرة واحدة بهذه الطريقة.
// عند إنشاء مخطط جديد ، فهذه هي الطريقة لمسح جميع البيانات التجريبية
// قبل أن نبدأ العمل على مخطط فارغ.
chartData.Clear();
```

### أنظر أيضا

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartseriescollection/)
* المجسم [Aspose.Words](../../../)


