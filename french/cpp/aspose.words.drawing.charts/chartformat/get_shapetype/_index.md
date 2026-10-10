---
title: "Méthode Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType"
linktitle: "get_ShapeType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType. Obtient ou définit le type de forme de l'élément de graphique parent en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.drawing.charts/chartformat/get_shapetype/
---
## ChartFormat::get_ShapeType method


Obtient ou définit le type de forme de l'élément de graphique parent.

```cpp
Aspose::Words::Drawing::Charts::ChartShapeType Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType()
```


## Exemples



Montre comment définir le remplissage, le contour et le formatage des infobulles pour les étiquettes de données du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une nouvelle série.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2", u"AW Category 3", u"AW Category 4"}), System::MakeArray<double>({100, 200, 300, 400}));

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);

// Formater les étiquettes de données en infobulles.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> format = series->get_DataLabels()->get_Format();
format->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::WedgeRectCallout);
format->get_Stroke()->set_Color(System::Drawing::Color::get_DarkGreen());
format->get_Fill()->Solid(System::Drawing::Color::get_Green());
series->get_DataLabels()->get_Font()->set_Color(System::Drawing::Color::get_Yellow());

// Modifier le remplissage et le contour d'une étiquette de données individuelle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> labelFormat = series->get_DataLabels()->idx_get(0)->get_Format();
labelFormat->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());
labelFormat->get_Fill()->Solid(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.FormatDataLables.docx");
```

## Voir aussi

* Enum [ChartShapeType](../../chartshapetype/)
* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
