---
title: get_Format
second_title: Aspose.Words for C++ API Reference
description: Provides access to fill and line formatting of the series.
type: docs
weight: 66
url: /cpp/aspose.words.drawing.charts/chartseries/get_format/
---
## ChartSeries::get_Format method


Provides access to fill and line formatting of the series.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartSeries::get_Format()
```


## Examples



Sows how to set series color. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Column, 432, 252);

SharedPtr<Chart> chart = shape->get_Chart();
SharedPtr<ChartSeriesCollection> seriesColl = chart->get_Series();

// Delete default generated series.
seriesColl->Clear();

// Create category names array.
auto categories = MakeArray<String>({u"Category 1", u"Category 2"});

// Adding new series. Value and category arrays must be the same size.
SharedPtr<ChartSeries> series1 = seriesColl->Add(u"Series 1", categories, MakeArray<double>({1, 2}));
SharedPtr<ChartSeries> series2 = seriesColl->Add(u"Series 2", categories, MakeArray<double>({3, 4}));
SharedPtr<ChartSeries> series3 = seriesColl->Add(u"Series 3", categories, MakeArray<double>({5, 6}));

// Set series color.
series1->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series2->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
series3->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(ArtifactsDir + u"Charts.SeriesColor.docx");
```

## See Also

* Class [ChartFormat](../../chartformat/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
