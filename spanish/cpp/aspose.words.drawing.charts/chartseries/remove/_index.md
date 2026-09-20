---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove method"
linktitle: "Remove"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove method. Elimina el valor X, el valor Y y el tamaño de burbuja, si es compatible, de la serie del gráfico en el índice especificado. El punto de datos y la etiqueta de datos correspondientes también se eliminan en C++."
type: docs
weight: 14500
url: /es/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


Elimina el valor X, el valor Y y el tamaño de burbuja, si están soportados, de la serie de gráfico en el índice indicado. También se elimina el punto de datos y la etiqueta de datos correspondientes.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## Ejemplos



Mostrar cómo agregar/eliminar valores de datos del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Eliminar el primer valor en ambas series.
department1Series->Remove(0);
department2Series->Remove(0);

// Añadir nuevos valores a ambas series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## Ver también

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
