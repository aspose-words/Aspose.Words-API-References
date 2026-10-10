---
title: "Aspose::Words::Drawing::Charts::ChartYValue clase"
linktitle: "ChartYValue"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartYValue clase. Representa un valor Y para una serie de gráfico en C++."
type: docs
weight: 18600
url: /es/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


Representa un valor Y para una serie de gráfico.

```cpp
class ChartYValue : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Obtiene una bandera que indica si el objeto especificado es igual al objeto de valor Y actual. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Crea una instancia de [ChartYValue](./) del tipo [DateTime](../chartyvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Crea una instancia de [ChartYValue](./) del tipo [Double](../chartyvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Crea una instancia de [ChartYValue](./) del tipo [Time](../chartyvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Obtiene el valor datetime almacenado. |
| [get_DoubleValue](./get_doublevalue/)() const | Obtiene el valor numérico almacenado. |
| [get_TimeValue](./get_timevalue/)() const | Obtiene el valor time almacenado. |
| [get_ValueType](./get_valuetype/)() const | Obtiene el tipo del valor Y almacenado en el objeto. |
| [GetHashCode](./gethashcode/)() const override | Obtiene un código hash para el objeto de valor Y actual. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Observaciones


Esta clase contiene varios métodos estáticos para crear un valor Y de un tipo particular. La propiedad [ValueType](./get_valuetype/) le permite determinar el tipo de un valor Y existente.

Todos los valores Y no nulos de una serie de gráfico deben ser del mismo tipo [ChartYValueType](../chartyvaluetype/).
## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
