---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale método"
linktitle: "get_BubbleScale"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale método. Obtiene o establece el tamaño de las burbujas como un porcentaje de su tamaño predeterminado en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Obtiene o establece el tamaño de las burbujas como un porcentaje de su tamaño predeterminado.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Observaciones


Se aplica solo a los grupos de series de los tipos [Bubble](../../chartseriestype/) y [Bubble3D](../../chartseriestype/).

El rango de valores aceptables es de 0 a 300 inclusive. El valor predeterminado es 100.

## Ejemplos



Muestra cómo establecer el tamaño de las burbujas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un gráfico de burbujas 3D.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Establece la escala de la burbuja al 200%.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## Ver también

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
