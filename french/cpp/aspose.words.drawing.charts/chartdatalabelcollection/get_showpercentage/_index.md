---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage méthode"
linktitle: "get_ShowPercentage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage méthode. Permet de spécifier si la valeur de pourcentage doit être affichée pour les étiquettes de données de l'ensemble de la série. La valeur par défaut est false. S'applique uniquement aux graphiques circulaires en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showpercentage/
---
## ChartDataLabelCollection::get_ShowPercentage method


Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de la série entière. La valeur par défaut est **false**. S'applique uniquement aux graphiques circulaires.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage()
```


## Exemples



Montre comment travailler avec les étiquettes de données d'un graphique circulaire.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Insérez une série de graphique personnalisée avec un nom de catégorie pour chaque secteur, ainsi que leur tableau de fréquences.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// Activez les étiquettes de données qui afficheront à la fois le pourcentage et la fréquence de chaque secteur, et modifiez leur apparence.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## Voir aussi

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
