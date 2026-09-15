---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top طريقة"
linktitle: "get_Top"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top طريقة. يحصل أو يضبط مسافة تسمية البيانات بالنقاط من الحافة العلوية للمخطط أو من الموضع المحدد بواسطة خاصية Position الخاصة به، اعتمادًا على قيمة خاصية TopMode في C++."
type: docs
weight: 16334
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabel/get_top/
---
## ChartDataLabel::get_Top method


يحصل أو يضبط مسافة تسمية البيانات بالنقاط من الحافة العليا للمخطط أو من الموضع المحدد بواسطة خاصية [Position](../get_position/) الخاصة به، اعتمادًا على قيمة خاصية [TopMode](../get_topmode/).

```cpp
double Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top()
```

## ملاحظات


تتغير قيمة الخاصية بشكل متناسب إذا تم تغيير حجم شكل المخطط.

لا يمكن ضبط الخاصية في مخطط Word 2016.

## أمثلة



يوضح كيفية وضع ملصقات البيانات لمخطط الدونات خارج الدونات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// حذف السلسلة التي تم إنشاؤها افتراضيًا.
seriesColl->Clear();

// إخفاء وسيلة الإيضاح.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// إنشاء البيانات.
const int32_t dataLength = 20;
double totalValue = 0;
auto categories = System::MakeArray<System::String>(dataLength);
auto values = System::MakeArray<double>(dataLength, 0);

for (int32_t i = 0; i < dataLength; i++)
{
    categories[i] = System::String::Format(u"Category {0}", i);
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", categories, values);
series->set_HasDataLabels(true);

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->set_ShowLeaderLines(true);

// لا يمكن استخدام خاصية Position للرسوم البيانية الدائرية. لنقم بوضع تسميات البيانات باستخدام Left و Top
// خصائص حول دائرة خارج الرسم البياني الدائري
// النقطة الأصلية في الزاوية العليا اليسرى من الرسم البياني.

const double titleAreaHeight = 25.5;
// يمكن حساب ذلك باستخدام نص العنوان والخط.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// يمكن حساب ذلك باستخدام خط التسمية.
const double oneCharLabelWidth = 12.75;
// يمكن حساب ذلك لكل تسمية باستخدام نصها والخط الخاص بها.
const double twoCharLabelWidth = 17.25;
// يمكن حساب ذلك لكل تسمية باستخدام نصها والخط الخاص بها.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// نظرًا لأن نقاط البيانات تبدأ من الأعلى، فإن إحداثيات X المستخدمة في خصائص Left و Top من
// تُشير تسميات البيانات إلى اليمين وإحداثيات Y تشير إلى الأسفل، الزاوية الابتدائية هي -PI/2.
double totalAngle = -System::Math::PI / 2;
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> previousLabel;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> dataLabel = dataLabels->idx_get(i);

    double value = series->get_YValues()->idx_get(i)->get_DoubleValue();
    double labelWidth;
    if (value < 10)
    {
        labelWidth = oneCharLabelWidth;
    }
    else
    {
        labelWidth = twoCharLabelWidth;
    }
    double labelSegmentAngle = value / totalValue * 2 * System::Math::PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System::Math::Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System::Math::Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // إذا كانت تسمية البيانات الحالية تتداخل مع تسميات أخرى، فقم بتحريكها أفقيًا.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // تحرك إلى اليمين في الأعلى، وإلى اليسار في الأسفل.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System::Math::PI);
        int32_t factor;
        if (isOnTop)
        {
            factor = 1;
        }
        else
        {
            factor = -1;
        }

        labelLeft = previousLabel->get_Left() + labelWidth * factor + labelMargin;
    }

    dataLabel->set_Left(labelLeft);
    dataLabel->set_LeftMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);
    dataLabel->set_Top(labelTop);
    dataLabel->set_TopMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChartLabelPosition.docx");
```

## انظر أيضًا

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
