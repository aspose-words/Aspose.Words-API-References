---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode método"
linktitle: "get_TopMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode método. Obtiene o establece el modo de interpretación del valor de la propiedad Top: si establece la ubicación de la etiqueta de datos desde el borde superior del gráfico o desde la posición especificada por su propiedad Position en C++."
type: docs
weight: 16667
url: /es/cpp/aspose.words.drawing.charts/chartdatalabel/get_topmode/
---
## ChartDataLabel::get_TopMode method


Obtiene o establece el modo de interpretación del valor de la propiedad [Top](../get_top/): si establece la ubicación de la etiqueta de datos desde el borde superior del gráfico o desde la posición especificada por su propiedad [Position](../get_position/).

```cpp
Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode()
```


## Ejemplos



Muestra cómo colocar las etiquetas de datos de un gráfico de rosquilla fuera de la rosquilla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Eliminar la serie generada por defecto.
seriesColl->Clear();

// Ocultar la leyenda.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Generar datos.
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

// La propiedad Position no se puede usar para gráficos de dona. Coloquemos las etiquetas de datos usando Left y Top
// propiedades alrededor de un círculo fuera de la dona del gráfico.
// El origen está en la esquina superior izquierda del gráfico.

const double titleAreaHeight = 25.5;
// Esto se puede calcular usando el texto del título y la fuente.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// Esto se puede calcular usando la fuente de la etiqueta.
const double oneCharLabelWidth = 12.75;
// Esto se puede calcular para cada etiqueta usando su texto y fuente.
const double twoCharLabelWidth = 17.25;
// Esto se puede calcular para cada etiqueta usando su texto y fuente.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Porque los puntos de datos comienzan en la parte superior, las coordenadas X usadas en las propiedades Left y Top de
// las etiquetas de datos apuntan a la derecha y las coordenadas Y apuntan hacia abajo, el ángulo inicial es -PI/2.
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

    // Si la etiqueta de datos actual se superpone a otras etiquetas, muévala horizontalmente.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Mueve a la derecha en la parte superior, a la izquierda en la parte inferior.
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

## Ver también

* Enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
