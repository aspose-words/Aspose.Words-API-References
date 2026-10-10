---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation méthode"
linktitle: "get_Rotation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation méthode. Obtient ou définit la rotation des étiquettes d'axe en degrés en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.drawing.charts/axisticklabels/get_rotation/
---
## AxisTickLabels::get_Rotation method


Obtient ou définit la rotation des étiquettes de marques en degrés.

```cpp
int32_t Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation()
```


## Exemples



Montre comment changer l'orientation et la rotation des étiquettes d'axe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un graphique en colonnes.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Définir l'orientation et la rotation des étiquettes d'axe.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## Voir aussi

* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
