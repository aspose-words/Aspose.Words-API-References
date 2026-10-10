---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation método"
linktitle: "get_Orientation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation método. Obtiene o establece la orientación del texto de la etiqueta de marca en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing.charts/axisticklabels/get_orientation/
---
## AxisTickLabels::get_Orientation method


Obtiene o establece la orientación del texto de la etiqueta de la marca de graduación.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation()
```

## Observaciones


El valor predeterminado es [Horizontal](../../../aspose.words.drawing/shapetextorientation/).

Tenga en cuenta que algunos valores de [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) no afectan la orientación del texto de la etiqueta de marca en los ejes de valores.

## Ejemplos



Muestra cómo cambiar la orientación y rotación de las etiquetas de marcas del eje.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un gráfico de columnas.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Establezca la orientación y rotación de las etiquetas de marcas del eje.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## Ver también

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
