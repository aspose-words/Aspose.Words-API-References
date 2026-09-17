---
title: "Méthode Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName"
linktitle: "get_ShowCategoryName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName. Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données de toute la série. La valeur par défaut est false en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showcategoryname/
---
## ChartDataLabelCollection::get_ShowCategoryName method


Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données de la série entière. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName()
```


## Exemples



Montre comment travailler avec les étiquettes de données d'un graphique à bulles.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Ajoutez une série personnalisée avec les coordonnées X/Y et le diamètre de chaque bulle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Activez les étiquettes de données, puis modifiez leur apparence.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```

## Voir aussi

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
