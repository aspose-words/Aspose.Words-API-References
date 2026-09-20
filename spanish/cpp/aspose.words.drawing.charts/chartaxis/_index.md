---
title: "Clase Aspose::Words::Drawing::Charts::ChartAxis"
linktitle: "ChartAxis"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::ChartAxis. Representa las opciones de eje del gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Representa las opciones del eje del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Obtiene o establece una bandera que indica si el eje de valores cruza el eje de categorías entre categorías. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Obtiene o establece la unidad de tiempo más pequeña que se representa en el eje de categorías de tiempo. |
| [get_CategoryType](./get_categorytype/)() | Obtiene o establece el tipo del eje de categorías. |
| [get_Crosses](./get_crosses/)() | Especifica cómo este eje cruza el eje perpendicular. |
| [get_CrossesAt](./get_crossesat/)() | Especifica dónde en el eje perpendicular cruza el eje. |
| [get_DisplayUnit](./get_displayunit/)() | Especifica el valor de escala de las unidades de visualización para el eje de valores. |
| [get_Document](./get_document/)() | Devuelve el documento que contiene el gráfico principal. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de línea del eje y al relleno de las etiquetas de marcas. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Obtiene o establece una bandera que indica si el eje tiene líneas de cuadrícula principales. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Obtiene o establece una bandera que indica si el eje tiene líneas de cuadrícula secundarias. |
| [get_Hidden](./get_hidden/)() | Obtiene o establece una bandera que indica si este eje está oculto o no. |
| [get_MajorTickMark](./get_majortickmark/)() | Obtiene o establece las marcas de graduación principales. |
| [get_MajorUnit](./get_majorunit/)() | Obtiene o establece la distancia entre las marcas de graduación principales. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Obtiene o establece una bandera que indica si se debe usar la distancia predeterminada entre las marcas de graduación principales. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Obtiene o establece el valor de escala para las marcas de graduación principales en el eje de categorías de tiempo. |
| [get_MinorTickMark](./get_minortickmark/)() | Obtiene o establece las marcas de graduación secundarias para el eje. |
| [get_MinorUnit](./get_minorunit/)() | Obtiene o establece la distancia entre las marcas de graduación secundarias. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Obtiene o establece una bandera que indica si se debe usar la distancia predeterminada entre las marcas de graduación secundarias. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Obtiene o establece el valor de escala para las marcas de graduación secundarias en el eje de categorías de tiempo. |
| [get_NumberFormat](./get_numberformat/)() | Devuelve un objeto [ChartNumberFormat](../chartnumberformat/) que permite definir formatos numéricos para el eje. |
| [get_ReverseOrder](./get_reverseorder/)() | Obtiene o establece una bandera que indica si los valores del eje deben mostrarse en orden inverso, es decir, de máximo a mínimo. |
| [get_Scaling](./get_scaling/)() | Proporciona acceso a las opciones de escala del eje. |
| [get_TickLabels](./get_ticklabels/)() | Proporciona acceso a las propiedades de las etiquetas de marcas de graduación del eje. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | Obtiene o establece el intervalo en el que se dibujan las marcas de graduación. |
| [get_Title](./get_title/)() | Proporciona acceso a las propiedades del título del eje. |
| [get_Type](./get_type/)() const | Devuelve el tipo del eje. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/). |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/). |
| [set_Hidden](./set_hidden/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Establecedor de [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo insertar un gráfico y modificar la apariencia de sus ejes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Inserte una serie de gráfico con categorías para el eje X y los valores numéricos respectivos para el eje Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Los ejes del gráfico tienen varias opciones que pueden cambiar su apariencia,
// como su dirección, marcas de unidad mayor/menor y marcas de graduación.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// Los gráficos de columnas no tienen eje Z.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
