---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top-Methode"
linktitle: "get_Top"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top-Methode. Ruft den Abstand der Datenbeschriftung in Punkten vom oberen Rand des Diagramms oder von der durch die Position‑Eigenschaft angegebenen Position ab oder legt ihn fest, abhängig vom Wert der TopMode‑Eigenschaft in C++."
type: docs
weight: 16334
url: /de/cpp/aspose.words.drawing.charts/chartdatalabel/get_top/
---
## ChartDataLabel::get_Top method


Ruft den Abstand der Datenbeschriftung in Punkten vom oberen Rand des Diagramms oder von der durch die [Position](../get_position/)-Eigenschaft angegebenen Position ab oder legt ihn fest, abhängig vom Wert der [TopMode](../get_topmode/)-Eigenschaft.

```cpp
double Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top()
```

## Hinweise


Der Wert der Eigenschaft ändert sich proportional, wenn die Diagrammform geändert wird.

Die Eigenschaft kann in einem Word‑2016‑Diagramm nicht festgelegt werden.

## Beispiele



Zeigt, wie Datenbeschriftungen eines Donut‑Diagramms außerhalb des Donuts platziert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Lösche standardmäßig generierte Serie.
seriesColl->Clear();

// Legende ausblenden.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Daten generieren.
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

// Die Position‑Eigenschaft kann für Donut‑Diagramme nicht verwendet werden. Platzieren wir Datenbeschriftungen mit den Eigenschaften Left und Top.
// Eigenschaften um einen Kreis außerhalb des Diagramm‑Donuts.
// Der Ursprung befindet sich in der oberen linken Ecke des Diagramms.

const double titleAreaHeight = 25.5;
// Dies kann mit dem Titeltext und der Schriftart berechnet werden.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// Dies kann mit der Beschriftungsschriftart berechnet werden.
const double oneCharLabelWidth = 12.75;
// Dies kann für jede Beschriftung mit deren Text und Schriftart berechnet werden.
const double twoCharLabelWidth = 17.25;
// Dies kann für jede Beschriftung mit deren Text und Schriftart berechnet werden.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Da die Datenpunkte oben beginnen, werden die X‑Koordinaten, die in den Eigenschaften Left und Top von
// die Datenbeschriftungen nach rechts zeigen und die Y‑Koordinaten nach unten, ist der Startwinkel -PI/2.
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

    // Wenn die aktuelle Datenbeschriftung andere Beschriftungen überlappt, verschieben Sie sie horizontal.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Bewegen Sie sich oben nach rechts, unten nach links.
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

## Siehe auch

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
