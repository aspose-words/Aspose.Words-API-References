---
title: "Aspose::Words::Drawing::Charts::ChartXValueCollection Klasse"
linktitle: "ChartXValueCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartXValueCollection Klasse. Stellt eine Sammlung von X-Werten für eine Diagrammserie in C++ dar."
type: docs
weight: 18400
url: /de/cpp/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class


Stellt eine Sammlung von X‑Werten für eine Diagrammreihe dar.

```cpp
class ChartXValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() | Gibt die Anzahl der Elemente in dieser Sammlung zurück. |
| [get_FormatCode](./get_formatcode/)() | Liest oder legt den Formatcode fest, der auf die X-Werte angewendet wird. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Liest oder legt den X-Wert am angegebenen Index fest. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Liest oder legt den X-Wert am angegebenen Index fest. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Setter für [Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Hinweise


Alle Elemente der Sammlung, die nicht **null** sind, müssen denselben [ValueType](../chartxvalue/get_valuetype/) haben.

Die Sammlung erlaubt nur das Ändern von X-Werten. Um neue Werte zu einer Diagrammserie hinzuzufügen oder einzufügen oder Werte zu entfernen, können die entsprechenden Methoden der [ChartSeries](../chartseries/) Klasse verwendet werden.

## Beispiele



Zeigt, wie man Diagrammreihendaten abruft.
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
    // Löschen Sie das individuelle Format aller Datenpunkte.
    // Datenpunkte und Datenwerte stehen in Säulendiagrammen eins zu eins.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // Y-Wert abrufen.
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

// Farben der maximalen und minimalen Werte ändern.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
