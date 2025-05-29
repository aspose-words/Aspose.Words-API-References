---
title: ChartSeriesCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ChartSeriesCollection GetEnumerator—استرداد كائنات المعداد بكفاءة لمعالجة البيانات وتحليلها بشكل سلس.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartseriescollection/getenumerator/
---
## ChartSeriesCollection.GetEnumerator method

يعيد كائن المعداد.

```csharp
public IEnumerator<ChartSeries> GetEnumerator()
```

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
