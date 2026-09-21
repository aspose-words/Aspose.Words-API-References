---
title: "Aspose::Words::Drawing::Charts::ChartYValueCollection class"
linktitle: "ChartYValueCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartYValueCollection class. Representerar en samling av Y‑värden för en diagramserie i C++."
type: docs
weight: 18800
url: /sv/cpp/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class


Representerar en samling av Y‑värden för en diagramserie.

```cpp
class ChartYValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Count](./get_count/)() | Hämtar antalet objekt i denna samling. |
| [get_FormatCode](./get_formatcode/)() | Hämtar eller anger formatkoden som tillämpas på Y‑värdena. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar eller anger Y‑värdet på det angivna indexet. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Hämtar eller anger Y‑värdet på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Anmärkningar


Alla objekt i samlingen förutom **null** måste ha samma [ValueType](../chartyvalue/get_valuetype/).

Samlingen tillåter endast att ändra Y‑värden. För att lägga till eller infoga nya värden i en diagramserie, eller ta bort värden, kan lämpliga metoder i klassen [ChartSeries](../chartseries/) användas.

## Exempel



Visar hur man hämtar diagramseriedata.
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
    // Rensa individuellt format för alla datapunkter.
    // Datapunkter och datavärden är en‑till‑en i stapeldiagram.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // Hämta Y‑värde.
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

// Ändra färgerna för max‑ och minvärdena.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
