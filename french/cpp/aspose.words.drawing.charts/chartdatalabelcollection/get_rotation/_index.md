---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation méthode"
linktitle: "get_Rotation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation méthode. Obtient ou définit la rotation des étiquettes de données de l’ensemble de la série en degrés en C++."
type: docs
weight: 5667
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_rotation/
---
## ChartDataLabelCollection::get_Rotation method


Obtient ou définit la rotation des étiquettes de données de la série entière en degrés.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation()
```

## Remarques


L’intervalle des valeurs acceptables va de -180 à 180 inclus. La valeur par défaut est 0.

Si la valeur de [Orientation](../get_orientation/) est [Horizontal](../../../aspose.words.drawing/shapetextorientation/), les formes d’étiquette, si elles existent, sont tournées avec le texte de l’étiquette. Sinon, seul le texte de l’étiquette est tourné.

## Exemples



Montre comment changer l'orientation et la rotation des étiquettes de données.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Définir la forme de l'étiquette de données.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Définir l'orientation et la rotation de l'étiquette de données pour toute la série.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Modifier l'orientation et la rotation de la première étiquette de données.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Voir aussi

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
