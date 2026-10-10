---
title: "Aspose::Words::Drawing::Charts::ChartAxisCollection class"
linktitle: "ChartAxisCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisCollection class. Rappresenta una raccolta di assi del grafico in C++."
type: docs
weight: 5500
url: /it/cpp/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class


Rappresenta una raccolta di assi del grafico.

```cpp
class ChartAxisCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Count](./get_count/)() | Ottiene il numero di assi in questa raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene l'asse all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come lavorare con la raccolta degli assi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Nascondi le linee della griglia principale sugli assi Y primario e secondario.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
