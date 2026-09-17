---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation méthode"
linktitle: "get_Rotation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation méthode. Obtient ou définit la rotation du titre de l'axe en degrés en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.drawing.charts/chartaxistitle/get_rotation/
---
## ChartAxisTitle::get_Rotation method


Obtient ou définit la rotation du titre de l'axe en degrés.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation()
```


## Exemples



Montre comment définir l'orientation et la rotation des titres du graphique et des axes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Avant de définir les propriétés du titre, assurez-vous que ce titre sera affiché.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## Voir aussi

* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
