---
title: "Método Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden"
linktitle: "get_Hidden"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden. Obtiene o establece una bandera que indica si este eje está oculto o no en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


Obtiene o establece una bandera que indica si este eje está oculto o no.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## Ejemplos



Muestra cómo ocultar los ejes del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Agregue una serie personalizada con categorías para el eje X y valores decimales respectivos para el eje Y.
chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// Oculte los ejes del gráfico para simplificar la apariencia del mismo.
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.HideChartAxis.docx");
```

## Ver también

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
