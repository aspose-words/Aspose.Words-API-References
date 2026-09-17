---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove method"
linktitle: "Supprimer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove method. Supprime la valeur X, la valeur Y et la taille de bulle, si prise en charge, de la série de graphique à l'index spécifié. Le point de données et l'étiquette de données correspondants sont également supprimés en C++."
type: docs
weight: 14500
url: /fr/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


Supprime la valeur X, la valeur Y et la taille de la bulle, si prises en charge, de la série de graphique à l'index indiqué. Le point de données et l'étiquette de données correspondants sont également supprimés.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## Exemples



Montre comment ajouter/supprimer des valeurs de données de graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Supprime la première valeur dans les deux séries.
department1Series->Remove(0);
department2Series->Remove(0);

// Ajoute de nouvelles valeurs aux deux séries.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## Voir aussi

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
