---
title: Aspose::Words::Drawing::Charts::ChartAxis::get_Title method
linktitle: get_Title
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartAxis::get_Title method. Provides access to the axis title properties in C++.'
type: docs
weight: 28500
url: /cpp/aspose.words.drawing.charts/chartaxis/get_title/
---
## ChartAxis::get_Title method


Provides access to the axis title properties.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> Aspose::Words::Drawing::Charts::ChartAxis::get_Title()
```


## Examples



Shows how to set chart axis title. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Delete default generated series.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## See Also

* Class [ChartAxisTitle](../../chartaxistitle/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
