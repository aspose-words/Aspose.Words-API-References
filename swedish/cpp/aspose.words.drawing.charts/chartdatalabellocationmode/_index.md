---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode enum"
linktitle: "ChartDataLabelLocationMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode enum. Anger hur värdena som specificerar placeringen av en datalabel – egenskaperna Left och Top – tolkas i C++."
type: docs
weight: 27167
url: /sv/cpp/aspose.words.drawing.charts/chartdatalabellocationmode/
---
## ChartDataLabelLocationMode enum


Anger hur värdena som specificerar placeringen av en datalabel – [Left](../chartdatalabel/get_left/) och [Top](../chartdatalabel/get_top/) egenskaperna – tolkas.

```cpp
enum class ChartDataLabelLocationMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Offset | 0 | Placeringen av en datalabel specificeras med ett avstånd från den position som definieras av dess [Position](../chartdatalabel/get_position/) egenskap. |
| Absolut | 1 | Placeringen av en datalabel specificeras med absoluta koordinater, med början från diagrammets övre vänstra hörn. |


## Exempel



Visar hur man placerar datalabels för donutdiagram utanför donuten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Ta bort standardgenererad serie.
seriesColl->Clear();

// Dölj förklaringen.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Generera data.
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

// Position‑egenskapen kan inte användas för donutdiagram. Låt oss placera datalabels med hjälp av Left och Top
// egenskaper runt en cirkel utanför diagrammets donut.
// Origo är i diagrammets övre vänstra hörn.

const double titleAreaHeight = 25.5;
// Detta kan beräknas med hjälp av titeltext och teckensnitt.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// Detta kan beräknas med hjälp av etikettens teckensnitt.
const double oneCharLabelWidth = 12.75;
// Detta kan beräknas för varje etikett med hjälp av dess text och teckensnitt.
const double twoCharLabelWidth = 17.25;
// Detta kan beräknas för varje etikett med hjälp av dess text och teckensnitt.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Eftersom datapunkterna startar högst upp, används X-koordinaterna i egenskaperna Left och Top för
// datapunktetiketterna pekar åt höger och Y-koordinaterna pekar nedåt, startvinkeln är -PI/2.
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

    // Om den aktuella datapunktetiketten överlappar andra etiketter, flytta den horisontellt.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Flytta åt höger högst upp, åt vänster längst ner.
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

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
