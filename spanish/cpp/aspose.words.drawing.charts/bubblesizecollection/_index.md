---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. Representa una colección de tamaños de burbuja para una serie de gráfico en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Representa una colección de tamaños de burbujas para una serie de gráfico.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Count](./get_count/)() | Obtiene el número de elementos en esta colección. |
| [get_FormatCode](./get_formatcode/)() | Obtiene o establece el código de formato aplicado a los tamaños de burbuja. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene o establece el valor del tamaño de burbuja en el índice especificado. |
| [idx_set](./idx_set/)(int32_t, double) | Obtiene o establece el valor del tamaño de burbuja en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Método set para [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Observaciones


La colección permite solo cambiar los tamaños de burbuja. Para agregar o insertar nuevos valores a una serie de gráfico, o eliminar valores, se pueden usar los métodos apropiados de la clase [ChartSeries](../chartseries/).

Los valores de tamaño de burbuja vacíos se representan como **NaN**.

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
