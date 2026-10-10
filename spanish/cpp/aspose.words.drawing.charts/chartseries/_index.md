---
title: "Aspose::Words::Drawing::Charts::ChartSeries clase"
linktitle: "ChartSeries"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries clase. Representa las propiedades de la serie del gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Representa las propiedades de la serie del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Agrega el valor X especificado a la serie del gráfico. Si la serie admite valores Y y tamaños de burbuja, estarán vacíos para el valor X. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Agrega los valores X y Y especificados a la serie del gráfico. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Agrega el valor X especificado, el valor Y y el tamaño de la burbuja a la serie del gráfico. |
| [Clear](./clear/)() | Elimina todos los valores de datos de la serie del gráfico. El formato de todos los puntos de datos individuales y de las etiquetas de datos se borra. |
| [ClearValues](./clearvalues/)() | Elimina todos los valores de datos de la serie del gráfico conservando el formato de los puntos de datos y de las etiquetas de datos. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Copia el formato predeterminado del punto de datos del punto de datos con el índice especificado. |
| [get_Bubble3D](./get_bubble3d/)() override | Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado. |
| [get_BubbleSizes](./get_bubblesizes/)() | Obtiene una colección de tamaños de burbujas para esta serie del gráfico. |
| [get_DataLabels](./get_datalabels/)() | Especifica la configuración de las etiquetas de datos para toda la serie. |
| [get_DataPoints](./get_datapoints/)() const | Devuelve una colección de objetos de formato para todos los puntos de datos en esta serie. |
| [get_Explosion](./get_explosion/)() override | Especifica la cantidad que el punto de datos debe moverse desde el centro del pastel. Puede ser negativo; negativo significa que la propiedad no está establecida y no se debe aplicar explosión. Se aplica solo a gráficos de pastel. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y de línea de la serie. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Obtiene o establece una bandera que indica si las etiquetas de datos se muestran para la serie. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
| [get_LegendEntry](./get_legendentry/)() | Obtiene una entrada de leyenda para esta serie de gráfico. |
| [get_Marker](./get_marker/)() override | Especifica un marcador de datos. El marcador se crea automáticamente cuando se solicita. |
| [get_Name](./get_name/)() | Obtiene el nombre de la serie; si el nombre no se establece explícitamente, se genera usando el índice. Por defecto devuelve Serie más uno basado en el índice. |
| [get_SeriesType](./get_seriestype/)() | Obtiene el tipo de esta serie de gráfico. |
| [get_Smooth](./get_smooth/)() const | Permite especificar si la línea que conecta los puntos del gráfico debe suavizarse usando splines Catmull-Rom. |
| [get_XValues](./get_xvalues/)() | Obtiene una colección de valores X para esta serie de gráfico. |
| [get_YValues](./get_yvalues/)() | Obtiene una colección de valores Y para esta serie de gráfico. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Inserta el valor X especificado en la serie de gráfico en el índice indicado. Si la serie admite valores Y y tamaños de burbuja, estarán vacíos para el valor X. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Inserta los valores X y Y especificados en la serie de gráfico en el índice indicado. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Inserta el valor X, el valor Y y el tamaño de burbuja especificados en la serie de gráfico en el índice indicado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Elimina el valor X, el valor Y y el tamaño de burbuja, si están soportados, de la serie de gráfico en el índice indicado. También se elimina el punto de datos y la etiqueta de datos correspondientes. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Método set para [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Especifica la cantidad que el punto de datos debe moverse desde el centro del pastel. Puede ser negativo; negativo significa que la propiedad no está establecida y no se debe aplicar explosión. Se aplica solo a gráficos de pastel. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
| [set_Name](./set_name/)(const System::String\&) | Establece el nombre de la serie; si el nombre no se establece explícitamente, se genera usando el índice. Por defecto devuelve Serie más uno basado en el índice. |
| [set_Smooth](./set_smooth/)(bool) | Permite especificar si la línea que conecta los puntos del gráfico debe suavizarse usando splines Catmull-Rom. |
| static [Type](./type/)() |  |
## Ver también

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
