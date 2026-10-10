---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Enum Aspose::Words::Drawing::ShapeTextOrientation. Spécifie l'orientation du texte dans les formes en C++."
type: docs
weight: 37500
url: /fr/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Spécifie l’orientation du texte dans les formes.

```cpp
enum class ShapeTextOrientation
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Horizontal | 0 | Le texte est disposé horizontalement (lr-tb). |
| Vers le bas | 1 | Le texte est pivoté de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl). |
| Vers le haut | 2 | Le texte est pivoté de 90 degrés vers la gauche pour apparaître de bas en haut (bt-lr). |
| VerticalFarEast | 3 | Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est pivoté de 90 degrés vers la droite pour s'afficher de haut en bas (tb-rl-v). |
| VerticalRotatedFarEast | 4 | Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est pivoté de 90 degrés vers la droite pour s'afficher de haut en bas verticalement, puis de gauche à droite horizontalement (tb-lr-v). |
| WordArtVertical | 5 | Le texte est vertical, avec une lettre au-dessus de l'autre. |
| WordArtVerticalRightToLeft | 6 | Le texte est vertical, avec une lettre au-dessus de l'autre, puis de droite à gauche horizontalement. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
