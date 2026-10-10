---
title: "Método get_Axes de Aspose::Words::Drawing::Charts::Chart"
linktitle: "get_Axes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_Axes de Aspose::Words::Drawing::Charts::Chart. Obtiene una colección de todos los ejes de este gráfico en C++."
type: docs
weight: 1500
url: /es/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


Obtiene una colección de todos los ejes de este gráfico.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


## Ejemplos



Muestra cómo trabajar con la colección de ejes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Oculta las líneas de cuadrícula principales en los ejes Y primario y secundario.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## Ver también

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
