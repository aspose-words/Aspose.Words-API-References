---
title: Class ChartYValueCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartYValueCollection فصل. يمثل مجموعة من قيم Y لسلسلة مخططات.
type: docs
weight: 880
url: /ar/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

يمثل مجموعة من قيم Y لسلسلة مخططات.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | الحصول على عدد العناصر في هذه المجموعة. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | الحصول على قيمة Y أو تعيينها في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | يُرجع كائن العداد. |

### ملاحظات

جميع عناصر المجموعة بخلاف **باطل** يجب أن يكون له نفس الشيء[`ValueType`](../chartyvalue/valuetype/).

تسمح المجموعة بتغيير قيم Y فقط. لإضافة أو إدراج قيم جديدة إلى سلسلة مخططات، أو إزالة القيم، الطرق المناسبة لـ[`ChartSeries`](../chartseries/) يمكن استخدام الطبقة.

### أمثلة

يوضح كيفية الحصول على بيانات سلسلة المخططات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // مسح التنسيق الفردي لجميع نقاط البيانات.
    // نقاط البيانات وقيم البيانات تكون فردية في المخططات العمودية.
    series.DataPoints[i].ClearFormat();

    // احصل على قيمة Y.
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// تغيير ألوان القيم القصوى والدنيا.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### أنظر أيضا

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


