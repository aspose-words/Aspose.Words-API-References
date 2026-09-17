---
title: "Aspose::Words::Drawing::Charts::Chart::get_Axes méthode"
linktitle: "get_Axes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::Chart::get_Axes méthode. Obtient une collection de tous les axes de ce graphique en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


Obtient une collection de tous les axes de ce graphique.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


## Exemples



Montre comment travailler avec la collection d'axes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Masquez les lignes de grille majeures sur les axes Y primaires et secondaires.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## Voir aussi

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
