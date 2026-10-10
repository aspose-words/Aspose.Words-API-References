---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection klass"
linktitle: "ChartSeriesCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection klass. Representerar en samling av en ChartSeries. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class


Representerar en samling av en [ChartSeries](../chartseries/). För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeriesCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) | Lägger till en ny [ChartSeries](../chartseries/) i denna samling. Använd den här metoden för att lägga till serier till alla typer av stapel-, kolumn-, linje- och ytkartor. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) |  |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Lägger till en ny [ChartSeries](../chartseries/) i denna samling. Använd den här metoden för att lägga till serier till alla typer av spridningsdiagram. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) | Lägger till en ny [ChartSeries](../chartseries/) i denna samling. Använd den här metoden för att lägga till serier till alla typer av områdes-, radar- och aktiediagram. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Lägger till en ny [ChartSeries](../chartseries/) i denna samling. Använd den här metoden för att lägga till serier till alla typer av bubbeldiagram. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) | Lägger till en ny [ChartSeries](../chartseries/) i denna samling. Använd den här metoden för att lägga till serier som har flernivåkategorier för data. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&) | Lägger till en ny [ChartSeries](../chartseries/) i denna samling. Använd den här metoden för att lägga till serier till histogramdiagram. |
| [Clear](./clear/)() | Tar bort alla [ChartSeries](../chartseries/) från denna samling. |
| [get_Count](./get_count/)() | Returnerar antalet [ChartSeries](../chartseries/) i denna samling. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar en [ChartSeries](../chartseries/) på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Tar bort en [ChartSeries](../chartseries/) på det angivna indexet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man lägger till och tar bort seriedata i ett diagram.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett kolumndiagram som som standard innehåller tre serier med demodata.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Varje serie har fyra decimala värden: ett för var och en av de fyra kategorierna.
// Fyra kluster med tre kolumner kommer att representera dessa data.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Skriv ut namnet på varje serie i diagrammet.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// Det här är namnen på kategorierna i diagrammet.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// Vi kan lägga till en serie med nya värden för befintliga kategorier.
// Detta diagram kommer nu att innehålla fyra kluster med fyra kolumner.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// En diagramserie kan också tas bort efter index, så här.
// Detta kommer att ta bort en av de tre demonstrationsserierna som följde med diagrammet.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// Vi kan också rensa all diagramdata på en gång med den här metoden.
// När du skapar ett nytt diagram är detta sättet att radera all demonstrationsdata
// innan vi kan börja arbeta på ett tomt diagram.
chartData->Clear();
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
