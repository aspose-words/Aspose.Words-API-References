---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation metod"
linktitle: "get_Rotation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation metod. Hämtar eller anger rotationen för dataetiketterna för hela serien i grader i C++."
type: docs
weight: 5667
url: /sv/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_rotation/
---
## ChartDataLabelCollection::get_Rotation method


Hämtar eller anger rotationen för dataetiketterna i hela serien i grader.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation()
```

## Anmärkningar


Det tillåtna värdeintervallet är från -180 till 180 inklusive. Standardvärdet är 0.

Om värdet för [Orientation](../get_orientation/) är [Horizontal](../../../aspose.words.drawing/shapetextorientation/), roteras etikettformer, om de finns, tillsammans med etiketttexten. Annars roteras endast etiketttexten.

## Exempel



Visar hur man ändrar orientering och rotation för datamärkningar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Visa datamärkningar.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Definiera datamärkningsform.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Ställ in datamärkningens orientering och rotation för hela serien.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Ändra orientering och rotation för den första datamärkningen.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Se även

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
