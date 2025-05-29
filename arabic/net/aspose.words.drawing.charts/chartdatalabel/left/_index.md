---
title: ChartDataLabel.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words لـ .NET
description: اضبط خاصية ChartDataLabel (تسمية بيانات الرسم البياني لليسار) للتحكم في موضع تسميات البيانات على الرسم البياني. حسّن الوضوح والعرض بإعدادات مسافة دقيقة.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/left/
---
## ChartDataLabel.Left property

يحصل على أو يعين مسافة تسمية البيانات بالنقاط من الحافة اليسرى للرسم البياني أو من الموضع المحدد بواسطة[`Position`](../position/) الممتلكات، اعتمادا على قيمة[`LeftMode`](../leftmode/) الخاصية.

```csharp
public double Left { get; set; }
```

## ملاحظات

تتغير قيمة الخاصية بشكل متناسب إذا تم تغيير حجم شكل الرسم البياني.

لا يمكن تعيين الخاصية في مخطط Word 2016.

## أمثلة

يوضح كيفية وضع تسميات البيانات الخاصة بالمخطط الدائري خارج المخطط الدائري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
//حذف السلسلة المولدة افتراضيًا.
seriesColl.Clear();

//إخفاء الأسطورة.
chart.Legend.Position = LegendPosition.None;

// توليد البيانات.
const int dataLength = 20;
double totalValue = 0;
string[] categories = new string[dataLength];
double[] values = new double[dataLength];

for (int i = 0; i < dataLength; i++)
{
    categories[i] = $"Category {i}";
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

ChartSeries series = seriesColl.Add("Series 1", categories, values);
series.HasDataLabels = true;

ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.ShowLeaderLines = true;

// لا يمكن استخدام خاصية الموضع في المخططات الدائرية. لنضع تسميات البيانات باستخدام اليسار والأعلى.
// الخصائص حول الدائرة خارج مخطط الدونات.
// الأصل موجود في الزاوية اليسرى العليا من الرسم البياني.

const double titleAreaHeight = 25.5; //يمكن حساب ذلك باستخدام نص العنوان والخط.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; //يمكن حساب ذلك باستخدام خط التسمية.
const double oneCharLabelWidth = 12.75; //يمكن حساب ذلك لكل تسمية باستخدام النص والخط الخاص بها.
const double twoCharLabelWidth = 17.25; //يمكن حساب ذلك لكل تسمية باستخدام النص والخط الخاص بها.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// نظرًا لأن نقاط البيانات تبدأ من الأعلى، فإن إحداثيات X المستخدمة في خصائص اليسار والأعلى لـ
// تشير تسميات البيانات إلى اليمين وتشير إحداثيات Y إلى الأسفل، وزاوية البداية هي -PI/2.
double totalAngle = -System.Math.PI / 2;
ChartDataLabel previousLabel = null;

for (int i = 0; i < series.YValues.Count; i++)
{
    ChartDataLabel dataLabel = dataLabels[i];

    double value = series.YValues[i].DoubleValue;
    double labelWidth;
    if (value < 10)
        labelWidth = oneCharLabelWidth;
    else
        labelWidth = twoCharLabelWidth;
    double labelSegmentAngle = value / totalValue * 2 * System.Math.PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System.Math.Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System.Math.Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // إذا كانت تسمية البيانات الحالية تتداخل مع تسميات أخرى، فقم بنقلها أفقيًا.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // التحرك إلى اليمين في الأعلى، واليسار في الأسفل.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System.Math.PI);
        int factor;
        if (isOnTop)
            factor = 1;
        else
            factor = -1;

        labelLeft = previousLabel.Left + labelWidth * factor + labelMargin;
    }

    dataLabel.Left = labelLeft;
    dataLabel.LeftMode = ChartDataLabelLocationMode.Absolute;
    dataLabel.Top = labelTop;
    dataLabel.TopMode = ChartDataLabelLocationMode.Absolute;

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc.Save(ArtifactsDir + "Charts.DoughnutChartLabelPosition.docx");
```

### أنظر أيضا

* class [ChartDataLabel](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
