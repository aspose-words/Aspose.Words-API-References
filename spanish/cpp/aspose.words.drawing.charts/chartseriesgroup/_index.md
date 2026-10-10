---
title: "Clase Aspose::Words::Drawing::Charts::ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::ChartSeriesGroup. Representa las propiedades de un grupo de series de gráfico, es decir, las propiedades de series de gráfico del mismo tipo asociadas a los mismos ejes en C++."
type: docs
weight: 17334
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Representa las propiedades de un grupo de series de gráfico, es decir, las propiedades de series de gráfico del mismo tipo asociadas a los mismos ejes.

```cpp
class ChartSeriesGroup : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Obtiene o establece el grupo de ejes al que pertenece este grupo de series. |
| [get_AxisX](./get_axisx/)() | Proporciona acceso a las propiedades del eje X de este grupo de series. |
| [get_AxisY](./get_axisy/)() | Proporciona acceso a las propiedades del eje Y de este grupo de series. |
| [get_BubbleScale](./get_bubblescale/)() | Obtiene o establece el tamaño de las burbujas como un porcentaje de su tamaño predeterminado. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Obtiene o establece el tamaño del agujero del gráfico de rosquilla principal como un porcentaje. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Obtiene o establece el ángulo, en grados, de la primera porción del gráfico de pastel principal. |
| [get_GapWidth](./get_gapwidth/)() | Obtiene o establece el porcentaje del ancho de espacio entre los elementos del gráfico. |
| [get_Overlap](./get_overlap/)() | Obtiene o establece el porcentaje de cuánto se superponen las barras o columnas de la serie. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Obtiene o establece el tamaño de la sección secundaria del gráfico circular como un porcentaje. |
| [get_Series](./get_series/)() | Obtiene una colección de series que pertenecen a este grupo de series. |
| [get_SeriesType](./get_seriestype/)() | Obtiene el tipo de series de gráfico incluidas en este grupo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Establecedor para [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Observaciones


Los gráficos combinados contienen varios grupos de series de gráficos, con un grupo separado para cada tipo de serie.

Además, puede crear un grupo de series de gráficos para asignar ejes secundarios a una o más series de gráficos.

Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

## Ejemplos



Muestra cómo trabajar con el eje secundario del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Eliminar la serie generada por defecto.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Crea un grupo de series adicional, también del tipo línea.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Especifique el uso de ejes secundarios para el nuevo grupo de series.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Oculta el eje X secundario.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Define el título del eje Y secundario.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Agrega una serie al nuevo grupo de series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
