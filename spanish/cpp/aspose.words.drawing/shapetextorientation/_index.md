---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeTextOrientation enum. Especifica la orientación del texto en formas en C++."
type: docs
weight: 37500
url: /es/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Especifica la orientación del texto en las formas.

```cpp
enum class ShapeTextOrientation
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | 0 | El texto se dispone horizontalmente (lr-tb). |
| Hacia abajo | 1 | El texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl). |
| Hacia arriba | 2 | El texto se rota 90 grados a la izquierda para aparecer de abajo a arriba (bt-lr). |
| VerticalFarEast | 3 | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl-v). |
| VerticalRotatedFarEast | 4 | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo verticalmente, luego de izquierda a derecha horizontalmente (tb-lr-v). |
| WordArtVertical | 5 | El texto es vertical, con una letra encima de la otra. |
| WordArtVerticalRightToLeft | 6 | El texto es vertical, con una letra encima de la otra, luego de derecha a izquierda horizontalmente. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
