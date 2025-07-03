---
title: Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add method
linktitle: Add
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add method. Adds new ChartSeries to this collection. Use this method to add series to Histogram charts in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing.charts/chartseriescollection/add/
---
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&) method


Adds new [ChartSeries](../../chartseries/) to this collection. Use this method to add series to Histogram charts.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues)
```


### ReturnValue

Recently added [ChartSeries](../../chartseries/) object.

## Examples



Shows how to create histogram chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Histogram chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Histogram, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Avg Temperature since 1991");

// Delete default generated series.
chart->get_Series()->Clear();

// Add a series.
chart->get_Series()->Add(u"Avg Temperature", System::MakeArray<double>({51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4, 53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7, 56.3, 55.9, 55.6}));

doc->Save(get_ArtifactsDir() + u"Charts.Histogram.docx");
```

## See Also

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) method


Adds new [ChartSeries](../../chartseries/) to this collection. Use this method to add series to any type of Scatter charts.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues, const System::ArrayPtr<double> &yValues)
```


### ReturnValue

Recently added [ChartSeries](../../chartseries/) object.

## See Also

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) method


Adds new [ChartSeries](../../chartseries/) to this collection. Use this method to add series to any type of Bubble charts.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues, const System::ArrayPtr<double> &yValues, const System::ArrayPtr<double> &bubbleSizes)
```


### ReturnValue

Recently added [ChartSeries](../../chartseries/) object.

## See Also

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) method


Adds new [ChartSeries](../../chartseries/) to this collection. Use this method to add series to any type of Area, Radar and Stock charts.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::DateTime> &dates, const System::ArrayPtr<double> &values)
```

## See Also

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) method


Adds new [ChartSeries](../../chartseries/) to this collection. Use this method to add series that have multi-level data categories.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>> &categories, const System::ArrayPtr<double> &values)
```


### ReturnValue

Recently added [ChartSeries](../../chartseries/) object.

## Examples



Shows how to create treemap chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Treemap chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Treemap, 450, 280);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"World Population");

// Delete default generated series.
chart->get_Series()->Clear();

// Add a series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Region", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"China"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"India"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Indonesia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Pakistan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Bangladesh"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Japan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Philippines"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Nigeria"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Ethiopia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Egypt"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Russia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Germany"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Brazil"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Mexico"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"United States", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Oceania")}), System::MakeArray<double>({1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000}));

// Show data labels.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowCategoryName(true);
System::String thousandSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyGroupSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"#{0}0", thousandSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Treemap.docx");
```


Shows how to create sunburst chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Sunburst chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Sunburst, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Sales");

// Delete default generated series.
chart->get_Series()->Clear();

// Add a series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Sales", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"London Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"Liverpool Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"Manchester Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"France", u"Paris Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"France", u"Lyon Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Denver Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Seattle Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Detroit Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Houston Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"Canada", u"Toronto Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"Canada", u"Montreal Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Oceania", u"Australia", u"Sydney Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Oceania", u"New Zealand", u"Auckland Dep.")}), System::MakeArray<double>({1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694}));

// Show data labels.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(false);
series->get_DataLabels()->set_ShowCategoryName(true);

doc->Save(get_ArtifactsDir() + u"Charts.Sunburst.docx");
```

## See Also

* Class [ChartSeries](../../chartseries/)
* Class [ChartMultilevelValue](../../chartmultilevelvalue/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) method


Adds new [ChartSeries](../../chartseries/) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::String> &categories, const System::ArrayPtr<double> &values)
```


### ReturnValue

Recently added [ChartSeries](../../chartseries/) object.

## Examples



Shows how to create pareto chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Pareto chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pareto, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Best-Selling Car");

// Delete default generated series.
chart->get_Series()->Clear();

// Add a series.
chart->get_Series()->Add(u"Best-Selling Car", System::MakeArray<System::String>({u"Tesla Model Y", u"Toyota Corolla", u"Toyota RAV4", u"Ford F-Series", u"Honda CR-V"}), System::MakeArray<double>({1.43, 0.91, 1.17, 0.98, 0.85}));

doc->Save(get_ArtifactsDir() + u"Charts.Pareto.docx");
```


Shows how to create box and whisker chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Box & Whisker chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::BoxAndWhisker, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Points by Years");

// Delete default generated series.
chart->get_Series()->Clear();

// Add a series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Points by Years", System::MakeArray<System::String>({u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA"}), System::MakeArray<double>({91, 80, 100, 77, 90, 104, 105, 118, 120, 101, 114, 107, 110, 60, 79, 78, 77, 102, 101, 113, 94, 93, 84, 71, 80, 103, 80, 94, 100, 101}));

// Show data labels.
series->set_HasDataLabels(true);

doc->Save(get_ArtifactsDir() + u"Charts.BoxAndWhisker.docx");
```


Shows how to create funnel chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Funnel chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Funnel, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Population by Age Group");

// Delete default generated series.
chart->get_Series()->Clear();

// Add a series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Age Group", System::MakeArray<System::String>({u"0-9", u"10-19", u"20-29", u"30-39", u"40-49", u"50-59", u"60-69", u"70-79", u"80-89", u"90-"}), System::MakeArray<double>({0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007}));

// Show data labels.
series->set_HasDataLabels(true);
System::String decimalSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyDecimalSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"0{0}0%", decimalSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Funnel.docx");
```

## See Also

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) method




```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::String> &categories, const System::ArrayPtr<double> &values, const System::ArrayPtr<bool> &isSubtotal)
```

## See Also

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
