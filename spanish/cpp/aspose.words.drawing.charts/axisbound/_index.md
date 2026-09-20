---
title: "Clase Aspose::Words::Drawing::Charts::AxisBound"
linktitle: "AxisBound"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::AxisBound. Representa el límite mínimo o máximo de los valores del eje. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Representa el límite mínimo o máximo de los valores del eje. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisBound : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [AxisBound](./axisbound/)() | Crea una nueva instancia que indica que el límite del eje debe determinarse automáticamente por una aplicación de procesamiento de textos. |
| [AxisBound](./axisbound/)(double) | Crea un límite de eje representado como un número. |
| [AxisBound](./axisbound/)(System::DateTime) | Crea un límite de eje representado como un valor de fecha y hora. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| [get_IsAuto](./get_isauto/)() const | Devuelve una bandera que indica que el límite del eje debe determinarse automáticamente. |
| [get_Value](./get_value/)() const | Devuelve el valor numérico del límite del eje. |
| [get_ValueAsDate](./get_valueasdate/)() | Devuelve el valor del límite del eje representado como fecha y hora. |
| [GetHashCode](./gethashcode/)() const override | Sirve como función hash para este tipo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Devuelve una cadena fácil de usar que muestra el valor de este objeto. |
| static [Type](./type/)() |  |
## Observaciones


El límite puede especificarse como un número, una fecha y hora o un valor especial "auto".

Las instancias de esta clase son inmutables.

## Ejemplos



Muestra cómo insertar un gráfico con valores de fecha/hora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Agrega una serie personalizada que contiene valores de fecha/hora para el eje X y valores decimales correspondientes para el eje Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// Establece los límites inferior y superior para el eje X.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// Establece las unidades principales del eje X a una semana y las unidades menores a un día.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// Define las propiedades del eje Y para valores decimales.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
