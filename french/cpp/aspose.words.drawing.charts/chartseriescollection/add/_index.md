---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add méthode"
linktitle: "Add"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add méthode. Ajoute un nouveau ChartSeries à cette collection. Utilisez cette méthode pour ajouter des séries aux graphiques Histogramme en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing.charts/chartseriescollection/add/
---
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&) method


Ajoute un nouveau [ChartSeries](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries aux graphiques Histogramme.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues)
```


### ReturnValue

Objet [ChartSeries](../../chartseries/) récemment ajouté.

## Exemples



Montre comment créer un graphique histogramme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un graphique Histogramme.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Histogram, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Avg Temperature since 1991");

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une série.
chart->get_Series()->Add(u"Avg Temperature", System::MakeArray<double>({51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4, 53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7, 56.3, 55.9, 55.6}));

doc->Save(get_ArtifactsDir() + u"Charts.Histogram.docx");
```

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) method


Ajoute un nouveau [ChartSeries](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques de dispersion.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues, const System::ArrayPtr<double> &yValues)
```


### ReturnValue

Objet [ChartSeries](../../chartseries/) récemment ajouté.

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) method


Ajoute un nouveau [ChartSeries](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques à bulles.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues, const System::ArrayPtr<double> &yValues, const System::ArrayPtr<double> &bubbleSizes)
```


### ReturnValue

Objet [ChartSeries](../../chartseries/) récemment ajouté.

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) method


Ajoute un nouveau [ChartSeries](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques de zone, radar et bourse.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::DateTime> &dates, const System::ArrayPtr<double> &values)
```

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) method


Ajoute un nouveau [ChartSeries](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries qui ont des catégories de données à plusieurs niveaux.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>> &categories, const System::ArrayPtr<double> &values)
```


### ReturnValue

Objet [ChartSeries](../../chartseries/) récemment ajouté.

## Exemples



Montre comment créer un graphique en carte d'arbres.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un graphique en carte d'arbres.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Treemap, 450, 280);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"World Population");

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une série.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Region", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"China"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"India"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Indonesia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Pakistan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Bangladesh"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Japan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Philippines"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Nigeria"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Ethiopia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Egypt"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Russia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Germany"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Brazil"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Mexico"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"United States", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Oceania")}), System::MakeArray<double>({1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000}));

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowCategoryName(true);
System::String thousandSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyGroupSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"#{0}0", thousandSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Treemap.docx");
```


Montre comment créer un graphique en rayons.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un graphique en rayons.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Sunburst, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Sales");

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une série.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Sales", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"London Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"Liverpool Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"Manchester Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"France", u"Paris Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"France", u"Lyon Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Denver Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Seattle Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Detroit Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Houston Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"Canada", u"Toronto Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"Canada", u"Montreal Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Oceania", u"Australia", u"Sydney Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Oceania", u"New Zealand", u"Auckland Dep.")}), System::MakeArray<double>({1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694}));

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(false);
series->get_DataLabels()->set_ShowCategoryName(true);

doc->Save(get_ArtifactsDir() + u"Charts.Sunburst.docx");
```

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartMultilevelValue](../../chartmultilevelvalue/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) method


Ajoute un nouveau [ChartSeries](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques à barres, colonnes, lignes et surfaces.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::String> &categories, const System::ArrayPtr<double> &values)
```


### ReturnValue

Objet [ChartSeries](../../chartseries/) récemment ajouté.

## Exemples



Montre comment créer un diagramme de Pareto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un diagramme de Pareto.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pareto, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Best-Selling Car");

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une série.
chart->get_Series()->Add(u"Best-Selling Car", System::MakeArray<System::String>({u"Tesla Model Y", u"Toyota Corolla", u"Toyota RAV4", u"Ford F-Series", u"Honda CR-V"}), System::MakeArray<double>({1.43, 0.91, 1.17, 0.98, 0.85}));

doc->Save(get_ArtifactsDir() + u"Charts.Pareto.docx");
```


Montre comment créer un diagramme à moustaches.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un diagramme Boîte & Moustaches.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::BoxAndWhisker, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Points by Years");

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une série.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Points by Years", System::MakeArray<System::String>({u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA"}), System::MakeArray<double>({91, 80, 100, 77, 90, 104, 105, 118, 120, 101, 114, 107, 110, 60, 79, 78, 77, 102, 101, 113, 94, 93, 84, 71, 80, 103, 80, 94, 100, 101}));

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);

doc->Save(get_ArtifactsDir() + u"Charts.BoxAndWhisker.docx");
```


Montre comment créer un diagramme en entonnoir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérer un diagramme en entonnoir.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Funnel, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Population by Age Group");

// Supprimer la série générée par défaut.
chart->get_Series()->Clear();

// Ajouter une série.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Age Group", System::MakeArray<System::String>({u"0-9", u"10-19", u"20-29", u"30-39", u"40-49", u"50-59", u"60-69", u"70-79", u"80-89", u"90-"}), System::MakeArray<double>({0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007}));

// Afficher les étiquettes de données.
series->set_HasDataLabels(true);
System::String decimalSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyDecimalSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"0{0}0%", decimalSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Funnel.docx");
```

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) method




```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::String> &categories, const System::ArrayPtr<double> &values, const System::ArrayPtr<bool> &isSubtotal)
```

## Voir aussi

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
