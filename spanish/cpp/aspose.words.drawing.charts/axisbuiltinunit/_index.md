---
title: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum"
linktitle: "AxisBuiltInUnit"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum. Especifica las unidades de visualización para un eje en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enum


Especifica las unidades de visualización para un eje.

```cpp
enum class AxisBuiltInUnit
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Especifica que los valores en el gráfico se mostrarán tal cual. |
| Personalizado | 1 | Especifica que los valores en el gráfico se dividirán por un divisor definido por el usuario. Este valor no es compatible con los nuevos tipos de gráficos de MS Office 2016. |
| Miles de millones | 2 | Especifica que los valores en el gráfico se dividirán por 1.000.000.000. |
| HundredMillions | 3 | Especifica que los valores en el gráfico se dividirán por 100.000.000. |
| Hundreds | 4 | Especifica que los valores en el gráfico se dividirán por 100. |
| HundredThousands | 5 | Especifica que los valores en el gráfico se dividirán por 100,000. |
| Millions | 6 | Especifica que los valores en el gráfico se dividirán por 1,000,000. |
| TenMillions | 7 | Especifica que los valores en el gráfico se dividirán por 10,000,000. |
| TenThousands | 8 | Especifica que los valores en el gráfico se dividirán por 10,000. |
| Thousands | 9 | Especifica que los valores en el gráfico se dividirán por 1,000. |
| Trillions | 10 | Especifica que los valores en el gráfico se dividirán por 1,000,000,000,0000. |
| Percentage | 11 | Especifica que los valores en el gráfico se dividirán por 0.01. Este valor solo es compatible con los nuevos tipos de gráficos de MS Office 2016. |


## Ejemplos



Muestra cómo manipular las marcas de graduación y los valores mostrados de un eje de gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Establezca las marcas de graduación menores del eje Y para que apunten fuera del área del gráfico,
// y las marcas de graduación mayores para que crucen el eje.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Establezca el eje Y para que muestre una marca mayor cada 10 unidades y una marca menor cada 1 unidad.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Establezca los límites del eje Y en -10 y 20.
// Este eje Y ahora mostrará 4 marcas mayores y 27 marcas menores.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// Para el eje X, establezca las marcas mayores cada 10 unidades,
// cada marca menor cada 2,5 unidades.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Configure ambos tipos de marcas de graduación para que aparezcan dentro del área del gráfico.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// Establezca los límites del eje X de modo que el eje X abarque 5 marcas mayores y 12 marcas menores.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// Establezca las etiquetas de marcas para que muestren su valor en millones.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// Podemos establecer un valor más específico por el cual las etiquetas de marcas mostrarán sus valores.
// Esta instrucción es equivalente a la anterior.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
