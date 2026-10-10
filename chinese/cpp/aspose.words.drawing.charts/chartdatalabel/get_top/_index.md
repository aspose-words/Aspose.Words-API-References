---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top 方法"
linktitle: "get_Top"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top 方法。获取或设置数据标签距离图表顶部边缘或其 Position 属性指定的位置的点数距离，取决于 TopMode 属性的值（在 C++ 中）。"
type: docs
weight: 16334
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabel/get_top/
---
## ChartDataLabel::get_Top method


获取或设置数据标签距离图表顶部边缘或其 [Position](../get_position/) 属性指定的位置的点数距离，取决于 [TopMode](../get_topmode/) 属性的值。

```cpp
double Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top()
```

## 备注


如果图表形状被重新调整大小，属性值会按比例变化。

在 Word 2016 图表中无法设置此属性。

## 示例



展示如何将环形图的数据标签放置在环形之外。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// 删除默认生成的系列。
seriesColl->Clear();

// 隐藏图例。
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// 生成数据。
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

// Position 属性不能用于环形图。让我们使用 Left 和 Top 来放置数据标签
// 属性围绕图表环形外部的圆圈。
// 原点位于图表的左上角。

const double titleAreaHeight = 25.5;
// 这可以使用标题文本和字体进行计算。
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// 这可以使用标签字体进行计算。
const double oneCharLabelWidth = 12.75;
// 这可以针对每个标签使用其文本和字体进行计算。
const double twoCharLabelWidth = 17.25;
// 这可以针对每个标签使用其文本和字体进行计算。
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// 由于数据点从顶部开始，Left 和 Top 属性中使用的 X 坐标
// 数据标签指向右侧，Y 坐标指向下方，起始角度为 -PI/2。
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

    // 如果当前数据标签与其他标签重叠，则水平移动它。
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // 在顶部向右移动，底部向左移动。
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

## 另见

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
