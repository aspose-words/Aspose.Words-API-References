---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_YValues méthode"
linktitle: "get_YValues"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_YValues méthode. Obtient une collection de valeurs Y pour cette série de graphique en C++."
type: docs
weight: 12667
url: /fr/cpp/aspose.words.drawing.charts/chartseries/get_yvalues/
---
## ChartSeries::get_YValues method


Obtient une collection de valeurs Y pour cette série de graphique.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValueCollection> Aspose::Words::Drawing::Charts::ChartSeries::get_YValues()
```


## Exemples



Montre comment travailler avec le code de format des données du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un graphique à bulles.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Définissez les codes de format des données.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## Voir aussi

* Class [ChartYValueCollection](../../chartyvaluecollection/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
