---
title: "classe Aspose::Words::Drawing::Charts::ChartYValueCollection"
linktitle: "ChartYValueCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Drawing::Charts::ChartYValueCollection. Rappresenta una raccolta di valori Y per una serie di grafico in C++."
type: docs
weight: 18800
url: /it/cpp/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class


Rappresenta una raccolta di valori Y per una serie di grafico.

```cpp
class ChartYValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Count](./get_count/)() | Restituisce il numero di elementi in questa raccolta. |
| [get_FormatCode](./get_formatcode/)() | Ottiene o imposta il codice di formato applicato ai valori Y. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta il valore Y all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Ottiene o imposta il valore Y all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Note


Tutti gli elementi della raccolta, eccetto **null**, devono avere lo stesso [ValueType](../chartyvalue/get_valuetype/).

La raccolta consente solo di modificare i valori Y. Per aggiungere o inserire nuovi valori a una serie di grafico, o rimuovere valori, è possibile utilizzare i metodi appropriati della classe [ChartSeries](../chartseries/).

## Esempi



Mostra come ottenere i dati della serie di grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->idx_get(0);

double minValue = std::numeric_limits<double>::max();
int32_t minValueIndex = 0;
double maxValue = std::numeric_limits<double>::lowest();
int32_t maxValueIndex = 0;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    // Cancella il formato individuale di tutti i punti dati.
    // I punti dati e i valori dei dati sono uno a uno nei grafici a colonne.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // Ottieni il valore Y.
    double yValue = series->get_YValues()->idx_get(i)->get_DoubleValue();

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

// Modifica i colori dei valori massimo e minimo.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
