---
title: "Aspose::Words::Drawing::Charts::Chart::get_Axes Methode"
linktitle: "get_Axes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::Chart::get_Axes method. Gibt eine Sammlung aller Achsen dieses Diagramms in C++ zurück."
type: docs
weight: 1500
url: /de/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


Gibt eine Sammlung aller Achsen dieses Diagramms zurück.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


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

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
