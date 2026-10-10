---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add 方法"
linktitle: "Add"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add 方法。向此集合添加新的 ChartSeries。使用此方法向直方图图表中添加系列（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing.charts/chartseriescollection/add/
---
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&) method


向此集合添加新的 [ChartSeries](../../chartseries/)。使用此方法向直方图图表中添加系列。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues)
```


### ReturnValue

最近添加的 [ChartSeries](../../chartseries/) 对象。

## 示例



展示如何创建直方图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入直方图。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Histogram, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Avg Temperature since 1991");

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加一个系列。
chart->get_Series()->Add(u"Avg Temperature", System::MakeArray<double>({51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4, 53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7, 56.3, 55.9, 55.6}));

doc->Save(get_ArtifactsDir() + u"Charts.Histogram.docx");
```

## 另见

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) method


向此集合添加新的 [ChartSeries](../../chartseries/)。使用此方法向任何类型的散点图添加系列。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues, const System::ArrayPtr<double> &yValues)
```


### ReturnValue

最近添加的 [ChartSeries](../../chartseries/) 对象。

## 另见

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) method


向此集合添加新的 [ChartSeries](../../chartseries/)。使用此方法向任何类型的气泡图添加系列。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<double> &xValues, const System::ArrayPtr<double> &yValues, const System::ArrayPtr<double> &bubbleSizes)
```


### ReturnValue

最近添加的 [ChartSeries](../../chartseries/) 对象。

## 另见

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) method


向此集合添加新的 [ChartSeries](../../chartseries/)。使用此方法向任何类型的面积图、雷达图和股票图添加系列。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::DateTime> &dates, const System::ArrayPtr<double> &values)
```

## 另见

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) method


向此集合添加新的 [ChartSeries](../../chartseries/)。使用此方法添加具有多级数据类别的系列。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>> &categories, const System::ArrayPtr<double> &values)
```


### ReturnValue

最近添加的 [ChartSeries](../../chartseries/) 对象。

## 示例



展示如何创建树状图表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个树状图表。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Treemap, 450, 280);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"World Population");

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加一个系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Region", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"China"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"India"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Indonesia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Pakistan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Bangladesh"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Japan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Philippines"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Nigeria"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Ethiopia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Egypt"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Russia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Germany"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Brazil"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Mexico"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"United States", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Oceania")}), System::MakeArray<double>({1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000}));

// 显示数据标签。
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowCategoryName(true);
System::String thousandSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyGroupSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"#{0}0", thousandSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Treemap.docx");
```


展示如何创建旭日图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入旭日图。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Sunburst, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Sales");

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加一个系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Sales", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"London Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"Liverpool Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"UK", u"Manchester Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"France", u"Paris Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Europe", u"France", u"Lyon Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Denver Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Seattle Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Detroit Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"USA", u"Houston Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"Canada", u"Toronto Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - NA", u"Canada", u"Montreal Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Oceania", u"Australia", u"Sydney Dep."), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Sales - Oceania", u"New Zealand", u"Auckland Dep.")}), System::MakeArray<double>({1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694}));

// 显示数据标签。
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(false);
series->get_DataLabels()->set_ShowCategoryName(true);

doc->Save(get_ArtifactsDir() + u"Charts.Sunburst.docx");
```

## 另见

* Class [ChartSeries](../../chartseries/)
* Class [ChartMultilevelValue](../../chartmultilevelvalue/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) method


向此集合添加新的 [ChartSeries](../../chartseries/)。使用此方法向任何类型的条形图、柱形图、折线图和曲面图添加系列。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::String> &categories, const System::ArrayPtr<double> &values)
```


### ReturnValue

最近添加的 [ChartSeries](../../chartseries/) 对象。

## 示例



展示如何创建帕累托图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入帕累托图。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pareto, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Best-Selling Car");

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加一个系列。
chart->get_Series()->Add(u"Best-Selling Car", System::MakeArray<System::String>({u"Tesla Model Y", u"Toyota Corolla", u"Toyota RAV4", u"Ford F-Series", u"Honda CR-V"}), System::MakeArray<double>({1.43, 0.91, 1.17, 0.98, 0.85}));

doc->Save(get_ArtifactsDir() + u"Charts.Pareto.docx");
```


展示如何创建箱线图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入箱线图。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::BoxAndWhisker, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Points by Years");

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加一个系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Points by Years", System::MakeArray<System::String>({u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"WC", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NR", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA", u"NA"}), System::MakeArray<double>({91, 80, 100, 77, 90, 104, 105, 118, 120, 101, 114, 107, 110, 60, 79, 78, 77, 102, 101, 113, 94, 93, 84, 71, 80, 103, 80, 94, 100, 101}));

// 显示数据标签。
series->set_HasDataLabels(true);

doc->Save(get_ArtifactsDir() + u"Charts.BoxAndWhisker.docx");
```


展示如何创建漏斗图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入漏斗图。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Funnel, 450, 450);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"Population by Age Group");

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加一个系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Age Group", System::MakeArray<System::String>({u"0-9", u"10-19", u"20-29", u"30-39", u"40-49", u"50-59", u"60-69", u"70-79", u"80-89", u"90-"}), System::MakeArray<double>({0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007}));

// 显示数据标签。
series->set_HasDataLabels(true);
System::String decimalSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyDecimalSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"0{0}0%", decimalSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Funnel.docx");
```

## 另见

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeriesCollection::Add(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) method




```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::Add(const System::String &seriesName, const System::ArrayPtr<System::String> &categories, const System::ArrayPtr<double> &values, const System::ArrayPtr<bool> &isSubtotal)
```

## 另见

* Class [ChartSeries](../../chartseries/)
* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
