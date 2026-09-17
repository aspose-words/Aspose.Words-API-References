---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format method"
linktitle: "get_Format"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format method. Fournit l'accès au remplissage et au format de ligne de la série en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing.charts/chartseries/get_format/
---
## ChartSeries::get_Format method


Fournit l'accès au remplissage et au formatage des lignes de la série.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartSeries::get_Format()
```


## Exemples



Montre comment définir la couleur de la série.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Supprimer la série générée par défaut.
seriesColl->Clear();

// Crée un tableau de noms de catégories.
auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});

// Ajout de nouvelles séries. Les tableaux de valeurs et de catégories doivent être de même taille.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = seriesColl->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = seriesColl->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = seriesColl->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));

// Définit la couleur de la série.
series1->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series2->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
series3->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.SeriesColor.docx");
```

## Voir aussi

* Class [ChartFormat](../../chartformat/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
