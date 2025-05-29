---
title: ChartSeriesCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى خاصية ChartSeriesCollection Item لاسترداد ChartSeries بسهولة حسب الفهرس، مما يعزز تجربة تصور البيانات لديك.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartseriescollection/item/
---
## ChartSeriesCollection indexer

يعيد[`ChartSeries`](../../chartseries/) عند الفهرس المحدد.

```csharp
public ChartSeries this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس للمجموعة. |

## ملاحظات

المؤشر يعتمد على الصفر.

يُسمح بالمؤشرات السلبية وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال، -1 يعني العنصر الأخير، -2 يعني العنصر الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فسوف يؤدي هذا إلى إرجاع مرجع فارغ.

إذا كان الفهرس سلبيًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فسيؤدي هذا إلى إرجاع مرجع فارغ.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
