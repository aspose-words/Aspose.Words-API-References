---
title: "Método Aspose::Words::DocumentBuilder::InsertChart"
linktitle: "InsertChart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::InsertChart. Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | El tipo de gráfico a insertar en el documento. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo especificar la posición y el ajuste al insertar un gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | El tipo de gráfico a insertar en el documento. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | El estilo del gráfico insertado. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double) method


Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | El tipo de gráfico a insertar en el documento. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar un gráfico circular en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Inserta un objeto de gráfico en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | El tipo de gráfico a insertar en el documento. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | El estilo del gráfico insertado. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
