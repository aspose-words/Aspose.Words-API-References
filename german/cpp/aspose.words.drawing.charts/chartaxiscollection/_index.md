---
title: "Aspose::Words::Drawing::Charts::ChartAxisCollection Klasse"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxisCollection Klasse. Stellt eine Sammlung von Diagrammachsen in C++ dar."
type: docs
weight: 5500
url: /de/cpp/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class


Stellt eine Sammlung von Diagrammachsen dar.

```cpp
class ChartAxisCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() | Liest die Anzahl der Achsen in dieser Sammlung. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Liest die Achse am angegebenen Index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man mit einer Achsensammlung arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Verstecke die großen Gitternetzlinien auf den primären und sekundären Y-Achsen.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
