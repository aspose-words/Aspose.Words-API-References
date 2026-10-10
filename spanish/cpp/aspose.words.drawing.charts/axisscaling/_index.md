---
title: "Clase Aspose::Words::Drawing::Charts::AxisScaling"
linktitle: "AxisScaling"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::AxisScaling. Representa las opciones de escalado del eje. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class


Representa las opciones de escala del eje. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisScaling : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [AxisScaling](./axisscaling/)() |  |
| [get_LogBase](./get_logbase/)() const | Obtiene o establece la base logarítmica para un eje logarítmico. |
| [get_Maximum](./get_maximum/)() | Obtiene o establece el valor máximo del eje. |
| [get_Minimum](./get_minimum/)() | Obtiene o establece el valor mínimo del eje. |
| [get_Type](./get_type/)() const | Obtiene o establece el tipo de escalado del eje. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_LogBase](./set_logbase/)(double) | Establecedor de [Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase](./get_logbase/). |
| [set_Maximum](./set_maximum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Establecedor de [Aspose::Words::Drawing::Charts::AxisScaling::get_Maximum](./get_maximum/). |
| [set_Minimum](./set_minimum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Establecedor de [Aspose::Words::Drawing::Charts::AxisScaling::get_Minimum](./get_minimum/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::Charts::AxisScaleType) | Establecedor de [Aspose::Words::Drawing::Charts::AxisScaling::get_Type](./get_type/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
