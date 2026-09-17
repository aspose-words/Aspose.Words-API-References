---
title: "Méthode Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Format"
linktitle: "get_Format"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Format. Fournit l'accès au remplissage et à la mise en forme des lignes des étiquettes de données en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_format/
---
## ChartDataLabelCollection::get_Format method


Fournit l'accès au formatage de remplissage et de ligne des étiquettes de données.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Format()
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

* Class [ChartFormat](../../chartformat/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
