---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartYValueCollection، الحل الأمثل لإدارة قيم Y في سلسلة المخططات بكفاءة وفعالية.
type: docs
weight: 1200
url: /ar/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

يمثل مجموعة من قيم Y لسلسلة الرسم البياني.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | يحصل على عدد العناصر في هذه المجموعة. |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | يحصل على رمز التنسيق المطبق على قيم Y أو يعينه. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | يحصل على قيمة Y أو يعينها عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | يعيد كائن المعداد. |

## ملاحظات

جميع عناصر المجموعة بخلاف**باطل** يجب أن يكون له نفس الشيء[`ValueType`](../chartyvalue/valuetype/).

تسمح المجموعة بتغيير قيم Y فقط. لإضافة أو إدراج قيم جديدة إلى سلسلة مخططات، أو إزالة قيم، استخدم الطرق المناسبة لـ[`ChartSeries`](../chartseries/) يمكن استخدام الفصل.

## أمثلة

يوضح كيفية الحصول على بيانات سلسلة الرسم البياني.

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
    // نقاط البيانات وقيم البيانات تكون متناسبة واحد لواحد في المخططات العمودية.
    series.DataPoints[i].ClearFormat();

    // الحصول على قيمة Y.
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

//تغيير ألوان القيم القصوى والدنيا.
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
