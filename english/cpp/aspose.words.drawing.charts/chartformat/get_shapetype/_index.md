---
title: Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType method
linktitle: get_ShapeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType method. Gets or sets the shape type of the parent chart element in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words.drawing.charts/chartformat/get_shapetype/
---
## ChartFormat::get_ShapeType method


Gets or sets the shape type of the parent chart element.

```cpp
Aspose::Words::Drawing::Charts::ChartShapeType Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType()
```


## Examples



Shows how to set fill, stroke and callout formatting for chart data labels. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Delete default generated series.
chart->get_Series()->Clear();

// Add new series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2", u"AW Category 3", u"AW Category 4"}), System::MakeArray<double>({100, 200, 300, 400}));

// Show data labels.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);

// Format data labels as callouts.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> format = series->get_DataLabels()->get_Format();
format->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::WedgeRectCallout);
format->get_Stroke()->set_Color(System::Drawing::Color::get_DarkGreen());
format->get_Fill()->Solid(System::Drawing::Color::get_Green());
series->get_DataLabels()->get_Font()->set_Color(System::Drawing::Color::get_Yellow());

// Change fill and stroke of an individual data label.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> labelFormat = series->get_DataLabels()->idx_get(0)->get_Format();
labelFormat->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());
labelFormat->get_Fill()->Solid(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.FormatDataLables.docx");
```

## See Also

* Enum [ChartShapeType](../../chartshapetype/)
* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
