---
title: "Método Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType"
linktitle: "get_ShapeType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType. Obtiene o establece el tipo de forma del elemento de gráfico principal en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.drawing.charts/chartformat/get_shapetype/
---
## ChartFormat::get_ShapeType method


Obtiene o establece el tipo de forma del elemento de gráfico principal.

```cpp
Aspose::Words::Drawing::Charts::ChartShapeType Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType()
```


## Ejemplos



Muestra cómo establecer el relleno, el trazo y el formato de llamada para las etiquetas de datos del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Eliminar la serie generada por defecto.
chart->get_Series()->Clear();

// Agregar nueva serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2", u"AW Category 3", u"AW Category 4"}), System::MakeArray<double>({100, 200, 300, 400}));

// Mostrar etiquetas de datos.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);

// Formatear etiquetas de datos como llamadas.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> format = series->get_DataLabels()->get_Format();
format->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::WedgeRectCallout);
format->get_Stroke()->set_Color(System::Drawing::Color::get_DarkGreen());
format->get_Fill()->Solid(System::Drawing::Color::get_Green());
series->get_DataLabels()->get_Font()->set_Color(System::Drawing::Color::get_Yellow());

// Cambiar el relleno y el trazo de una etiqueta de datos individual.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> labelFormat = series->get_DataLabels()->idx_get(0)->get_Format();
labelFormat->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());
labelFormat->get_Fill()->Solid(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.FormatDataLables.docx");
```

## Ver también

* Enum [ChartShapeType](../../chartshapetype/)
* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
