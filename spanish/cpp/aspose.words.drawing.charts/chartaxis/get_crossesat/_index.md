---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt método"
linktitle: "get_CrossesAt"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt método. Especifica dónde en el eje perpendicular cruza el eje en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing.charts/chartaxis/get_crossesat/
---
## ChartAxis::get_CrossesAt method


Especifica dónde en el eje perpendicular cruza el eje.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt()
```

## Observaciones


La propiedad tiene efecto solo si [Crosses](../get_crosses/) está configurado a [Custom](../../axiscrosses/). No es compatible con los nuevos gráficos de MS Office 2016.

Las unidades se determinan por el tipo de eje. Cuando el eje es un eje de valores, el valor de la propiedad es un número decimal en el eje de valores. Cuando el eje es un eje de categoría de tiempo, el valor se define como un número entero de días relativo a la fecha base (30/12/1899). Para un eje de categoría de texto, el valor es un número entero de categoría, comenzando con 1 como la primera categoría.

## Ejemplos



Muestra cómo hacer que un eje de gráfico cruce en una ubicación personalizada.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Para los gráficos de columnas, el eje Y cruza en cero por defecto,
// lo que significa que las columnas para todos los valores por debajo de cero apuntan hacia abajo para representar valores negativos.
// Podemos establecer un valor diferente para el cruce del eje Y. En este caso, lo estableceremos en 3.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## Ver también

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
