---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::idx_get Methode. Gibt ein ChartSeries am angegebenen Index in C++ zurück."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing.charts/chartseriescollection/idx_get/
---
## ChartSeriesCollection::idx_get method


Gibt ein [ChartSeries](../../chartseries/) am angegebenen Index zurück.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Sammlung. |
## Hinweise


Der Index ist nullbasiert.

Negative Indizes sind erlaubt und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer als oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer ist als die Anzahl der Elemente in der Liste, gibt dies eine Nullreferenz zurück.

## Beispiele



Zeigt, wie man Seriendaten in einem Diagramm hinzufügt und entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Säulendiagramm ein, das standardmäßig drei Serien mit Beispieldaten enthält.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Jede Serie hat vier Dezimalwerte: einen für jede der vier Kategorien.
// Vier Cluster aus je drei Säulen stellen diese Daten dar.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Geben Sie den Namen jeder Serie im Diagramm aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// Dies sind die Namen der Kategorien im Diagramm.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// Wir können eine Serie mit neuen Werten für vorhandene Kategorien hinzufügen.
// Dieses Diagramm wird nun vier Cluster von vier Spalten enthalten.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// Eine Diagrammserie kann ebenfalls nach Index entfernt werden, wie folgt.
// Dies wird eine der drei Demo-Serien entfernen, die mit dem Diagramm geliefert wurden.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// Wir können auch alle Diagrammdaten auf einmal mit dieser Methode löschen.
// Beim Erstellen eines neuen Diagramms ist dies der Weg, alle Demo-Daten zu löschen
// bevor wir mit einem leeren Diagramm arbeiten können.
chartData->Clear();
```

## Siehe auch

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
