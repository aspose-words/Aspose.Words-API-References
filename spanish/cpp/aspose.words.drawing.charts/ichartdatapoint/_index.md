---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint interfaz"
linktitle: "IChartDataPoint"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint interfaz. Contiene propiedades de un único punto de datos en el gráfico en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Contiene propiedades de un único punto de datos en el gráfico.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado. |
| virtual [get_Explosion](./get_explosion/)() | Especifica la cantidad que el punto de datos debe moverse desde el centro del pastel. Puede ser negativo; negativo significa que la propiedad no está establecida y no se debe aplicar explosión. Se aplica solo a gráficos de pastel. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
| virtual [get_Marker](./get_marker/)() | Especifica un marcador de datos. El marcador se crea automáticamente cuando se solicita. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Establecedor para [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
