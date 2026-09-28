---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode метод"
linktitle: "get_LeftMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode метод. Получает или задает режим интерпретации значения свойства Left: определяет, устанавливает ли он расположение метки данных от левого края диаграммы или от позиции, указанной в свойстве Position, в C++."
type: docs
weight: 6667
url: /ru/cpp/aspose.words.drawing.charts/chartdatalabel/get_leftmode/
---
## ChartDataLabel::get_LeftMode method


Получает или задает режим интерпретации значения свойства [Left](../get_left/): определяет, устанавливает ли он расположение метки данных от левого края диаграммы или от позиции, указанной в свойстве [Position](../get_position/).

```cpp
Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode()
```


## Примеры



Показывает, как разместить подписи данных кольцевой диаграммы за её пределами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Удалить автоматически сгенерированную серию.
seriesColl->Clear();

// Скрыть легенду.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Сгенерировать данные.
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

// Свойство Position нельзя использовать для кольцевых диаграмм. Давайте разместим подписи данных, используя свойства Left и Top
// свойства вокруг круга за пределами кольцевой диаграммы.
// Начало координат находится в верхнем левом углу диаграммы.

const double titleAreaHeight = 25.5;
// Это можно вычислить, используя текст заголовка и шрифт.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// Это можно вычислить, используя шрифт подписи.
const double oneCharLabelWidth = 12.75;
// Это можно вычислить для каждой подписи, используя её текст и шрифт.
const double twoCharLabelWidth = 17.25;
// Это можно вычислить для каждой подписи, используя её текст и шрифт.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Поскольку точки данных начинаются сверху, координаты X, используемые в свойствах Left и Top
// подписи данных указывают вправо, а координаты Y — вниз, начальный угол равен -PI/2.
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

    // Если текущая подпись данных перекрывает другие подписи, переместите её горизонтально.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Переместите вправо вверху, влево внизу.
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

## См. также

* Enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
