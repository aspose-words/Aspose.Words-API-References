---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection class"
linktitle: "ChartSeriesCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection class. Stellt eine Sammlung von ChartSeries dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class


Stellt eine Sammlung von [ChartSeries](../chartseries/) dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeriesCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) | Fügt dieser Sammlung ein neues [ChartSeries](../chartseries/) hinzu. Verwenden Sie diese Methode, um Serien zu Diagrammen vom Typ Balken, Säule, Linie und Fläche hinzuzufügen. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) |  |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Fügt dieser Sammlung ein neues [ChartSeries](../chartseries/) hinzu. Verwenden Sie diese Methode, um Serien zu Streudiagrammen hinzuzufügen. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) | Fügt dieser Sammlung ein neues [ChartSeries](../chartseries/) hinzu. Verwenden Sie diese Methode, um Serien zu Flächen-, Radar- und Börsendiagrammen hinzuzufügen. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Fügt dieser Sammlung ein neues [ChartSeries](../chartseries/) hinzu. Verwenden Sie diese Methode, um Serien zu Blasendiagrammen hinzuzufügen. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) | Fügt dieser Sammlung ein neues [ChartSeries](../chartseries/) hinzu. Verwenden Sie diese Methode, um Serien mit mehrstufigen Datenkategorien hinzuzufügen. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&) | Fügt dieser Sammlung ein neues [ChartSeries](../chartseries/) hinzu. Verwenden Sie diese Methode, um Serien zu Histogrammdiagrammen hinzuzufügen. |
| [Clear](./clear/)() | Entfernt alle [ChartSeries](../chartseries/) aus dieser Sammlung. |
| [get_Count](./get_count/)() | Gibt die Anzahl der [ChartSeries](../chartseries/) in dieser Sammlung zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt ein [ChartSeries](../chartseries/) am angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Entfernt ein [ChartSeries](../chartseries/) am angegebenen Index. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
