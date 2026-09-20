---
title: "Método Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase"
linktitle: "get_LogBase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase. Obtiene o establece la base logarítmica para un eje logarítmico en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing.charts/axisscaling/get_logbase/
---
## AxisScaling::get_LogBase method


Obtiene o establece la base logarítmica para un eje logarítmico.

```cpp
double Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase() const
```

## Observaciones


La propiedad no es compatible con los nuevos gráficos de MS Office 2016.

El rango válido de un valor de punto flotante es mayor o igual a 2 y menor o igual a 1000. La propiedad tiene efecto solo si [Type](../get_type/) está configurado a [Logarithmic](../../axisscaletype/).

Establecer esta propiedad asigna la propiedad [Type](../get_type/) a [Logarithmic](../../axisscaletype/).

## Ejemplos



Muestra cómo aplicar escalado logarítmico a un eje del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Inserte una serie con coordenadas X/Y para cinco puntos.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// El escalado del eje X es lineal por defecto,
// mostrando valores incrementados uniformemente que cubren nuestro rango de valores X (0, 1, 2, 3...).
// Un eje lineal no es ideal para nuestros valores Y
// ya que los puntos con valores Y más pequeños serán más difíciles de leer.
// Un escalado logarítmico con una base de 20 (1, 20, 400, 8000...)
// distribuirá los puntos trazados, permitiéndonos leer sus valores en el gráfico más fácilmente.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## Ver también

* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
