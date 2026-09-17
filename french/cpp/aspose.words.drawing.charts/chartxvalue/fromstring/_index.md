---
title: "Aspose::Words::Drawing::Charts::ChartXValue::FromString méthode"
linktitle: "FromString"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartXValue::FromString method. Crée une instance de ChartXValue du type String en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing.charts/chartxvalue/fromstring/
---
## ChartXValue::FromString method


Crée une instance de [ChartXValue](../) du type [String](../../chartxvaluetype/) .

```cpp
static System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> Aspose::Words::Drawing::Charts::ChartXValue::FromString(const System::String &value)
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

* Class [ChartXValue](../)
* Class [ChartXValue](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
