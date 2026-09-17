---
title: "Méthode Aspose::Words::Drawing::Charts::Chart::get_Title"
linktitle: "get_Title"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::Chart::get_Title. Fournit l'accès aux propriétés du titre du graphique en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.drawing.charts/chart/get_title/
---
## Chart::get_Title method


Fournit l'accès aux propriétés du titre du graphique.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> Aspose::Words::Drawing::Charts::Chart::get_Title()
```


## Exemples



Montre comment insérer un graphique et définir un titre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une forme de graphique avec un constructeur de document et récupérez son graphique.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Utilisez la propriété "Title" pour donner à notre graphique un titre, qui apparaît au centre supérieur de la zone du graphique.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Définissez la propriété "Show" sur "true" pour rendre le titre visible.
title->set_Show(true);

// Définissez la propriété "Overlay" sur "true". Donnez plus d'espace aux autres éléments du graphique en leur permettant de chevaucher le titre.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Voir aussi

* Class [ChartTitle](../../charttitle/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
