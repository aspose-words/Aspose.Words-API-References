---
title: "Aspose::Words::Drawing::Charts::ChartXValue clase"
linktitle: "ChartXValue"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartXValue clase. Representa un valor X para una serie de gráfico en C++."
type: docs
weight: 18200
url: /es/cpp/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class


Representa un valor X para una serie de gráfico.

```cpp
class ChartXValue : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Obtiene una bandera que indica si el objeto especificado es igual al objeto de valor X actual. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | Crea una instancia de [ChartXValue](./) del tipo [DateTime](../chartxvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | Crea una instancia de [ChartXValue](./) del tipo [Double](../chartxvaluetype/). |
| static [FromMultilevelValue](./frommultilevelvalue/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\&) | Crea una instancia de [ChartXValue](./) del tipo [Multilevel](../chartxvaluetype/). |
| static [FromString](./fromstring/)(const System::String\&) | Crea una instancia de [ChartXValue](./) del tipo [String](../chartxvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | Crea una instancia de [ChartXValue](./) del tipo [Time](../chartxvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | Obtiene el valor datetime almacenado. |
| [get_DoubleValue](./get_doublevalue/)() const | Obtiene el valor numérico almacenado. |
| [get_MultilevelValue](./get_multilevelvalue/)() const | Obtiene el valor multilevel almacenado. |
| [get_StringValue](./get_stringvalue/)() const | Obtiene el valor string almacenado. |
| [get_TimeValue](./get_timevalue/)() const | Obtiene el valor time almacenado. |
| [get_ValueType](./get_valuetype/)() const | Obtiene el tipo del valor X almacenado en el objeto. |
| [GetHashCode](./gethashcode/)() const override | Obtiene un código hash para el objeto de valor X actual. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Observaciones


Esta clase contiene varios métodos estáticos para crear un valor X de un tipo particular. La propiedad [ValueType](./get_valuetype/) le permite determinar el tipo de un valor X existente.

Todos los valores X no nulos de una serie de gráfico deben ser del mismo tipo [ChartXValueType](../chartxvaluetype/).

## Ejemplos



Muestra cómo rellenar series de gráfico con datos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Borra los valores X e Y de la primera serie.
series1->ClearValues();

// Rellena la serie con datos.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Borra los valores X e Y de la segunda serie.
series2->Clear();

// Rellena la serie con datos.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
