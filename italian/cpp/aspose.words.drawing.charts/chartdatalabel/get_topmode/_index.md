---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode metodo"
linktitle: "get_TopMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode metodo. Ottiene o imposta la modalità di interpretazione del valore della proprietà Top: se imposta la posizione dell'etichetta dei dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà Position in C++."
type: docs
weight: 16667
url: /it/cpp/aspose.words.drawing.charts/chartdatalabel/get_topmode/
---
## ChartDataLabel::get_TopMode method


Ottiene o imposta la modalità di interpretazione del valore della proprietà [Top](../get_top/): se imposta la posizione dell'etichetta dei dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [Position](../get_position/).

```cpp
Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode()
```


## Esempi



Mostra come posizionare le etichette dati di un grafico a ciambella all'esterno della ciambella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Elimina la serie generata di default.
seriesColl->Clear();

// Nascondi la legenda.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Genera dati.
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

// La proprietà Position non può essere usata per i grafici a ciambella. Posizioniamo le etichette dei dati usando Left e Top
// proprietà intorno a un cerchio all'esterno della ciambella del grafico.
// L'origine si trova nell'angolo in alto a sinistra del grafico.

const double titleAreaHeight = 25.5;
// Questo può essere calcolato usando il testo del titolo e il carattere.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// Questo può essere calcolato usando il carattere dell'etichetta.
const double oneCharLabelWidth = 12.75;
// Questo può essere calcolato per ogni etichetta usando il suo testo e il carattere.
const double twoCharLabelWidth = 17.25;
// Questo può essere calcolato per ogni etichetta usando il suo testo e il carattere.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Poiché i punti dati iniziano in alto, le coordinate X usate nelle proprietà Left e Top di
// le etichette dei dati puntano a destra e le coordinate Y puntano verso il basso, l'angolo di partenza è -PI/2.
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

    // Se l'etichetta dati corrente si sovrappone ad altre etichette, spostala orizzontalmente.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Sposta a destra in alto, a sinistra in basso.
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

## Vedi anche

* Enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
