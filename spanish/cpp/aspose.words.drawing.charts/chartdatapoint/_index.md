---
title: "Clase Aspose::Words::Drawing::Charts::ChartDataPoint"
linktitle: "ChartDataPoint"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::ChartDataPoint. Permite especificar el formato de un único punto de datos en el gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Permite especificar el formato de un solo punto de datos en el gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormat](./clearformat/)() | Borra el formato de este punto de datos. Las propiedades se establecen a los valores predeterminados definidos en la serie principal. |
| [get_Bubble3D](./get_bubble3d/)() override | Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado. |
| [get_Explosion](./get_explosion/)() override | Especifica la cantidad que el punto de datos debe moverse desde el centro del pastel. Puede ser negativo; negativo significa que la propiedad no está establecida y no se debe aplicar explosión. Se aplica solo a gráficos de pastel. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y línea de este punto de datos. |
| [get_Index](./get_index/)() | Índice del punto de datos al que este objeto aplica el formato. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
| [get_Marker](./get_marker/)() override | Especifica el marcador de datos del gráfico. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado. |
| [set_Explosion](./set_explosion/)(int32_t) override | Establecedor para [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
| static [Type](./type/)() |  |
## Ver también

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
