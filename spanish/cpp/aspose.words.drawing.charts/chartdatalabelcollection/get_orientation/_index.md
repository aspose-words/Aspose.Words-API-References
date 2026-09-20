---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation método"
linktitle: "get_Orientation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation método. Obtiene o establece la orientación del texto de las etiquetas de datos de toda la serie en C++."
type: docs
weight: 5334
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_orientation/
---
## ChartDataLabelCollection::get_Orientation method


Obtiene o establece la orientación del texto de las etiquetas de datos de toda la serie.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation()
```


## Ejemplos



Muestra cómo cambiar la orientación y rotación de las etiquetas de datos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Mostrar etiquetas de datos.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Definir la forma de la etiqueta de datos.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Establecer la orientación y rotación de la etiqueta de datos para toda la serie.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Cambiar la orientación y rotación de la primera etiqueta de datos.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Ver también

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
