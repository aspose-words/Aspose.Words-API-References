---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion método"
linktitle: "get_Explosion"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion método. Especifica la cantidad que el punto de datos debe desplazarse desde el centro del gráfico de pastel. Puede ser negativo; negativo significa que la propiedad no está establecida y no se debe aplicar explosión. Aplica solo a gráficos de pastel en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing.charts/ichartdatapoint/get_explosion/
---
## IChartDataPoint::get_Explosion method


Especifica la cantidad que el punto de datos debe moverse desde el centro del pastel. Puede ser negativo; negativo significa que la propiedad no está establecida y no se debe aplicar explosión. Se aplica solo a gráficos de pastel.

```cpp
virtual int32_t Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion()=0
```


## Ejemplos



Muestra cómo mover las porciones de un gráfico de pastel alejándolas del centro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// "Slices" de un gráfico de pastel pueden moverse alejados del centro a una distancia mediante el atributo Explosion del punto de datos correspondiente.
// Agrega un punto de datos a la primera porción del gráfico de pastel y muévelo alejado del centro en 10 puntos.
// Aspose.Words crea puntos de datos automáticamente si no existen.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// Desplace la segunda porción a una distancia mayor.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## Ver también

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
