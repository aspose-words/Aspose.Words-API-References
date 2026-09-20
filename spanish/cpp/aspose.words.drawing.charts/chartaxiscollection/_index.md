---
title: "Clase Aspose::Words::Drawing::Charts::ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::ChartAxisCollection. Representa una colección de ejes de gráfico en C++."
type: docs
weight: 5500
url: /es/cpp/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class


Representa una colección de ejes del gráfico.

```cpp
class ChartAxisCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Count](./get_count/)() | Obtiene el número de ejes en esta colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene el eje en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
