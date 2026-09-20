---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class"
linktitle: "ChartDataLabelCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::ChartDataLabelCollection. Representa una colección de ChartDataLabel. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Representa una colección de [ChartDataLabel](../chartdatalabel/). Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormat](./clearformat/)() | Borra el formato de todos los [ChartDataLabel](../chartdatalabel/) en esta colección. |
| [get_Count](./get_count/)() | Devuelve el número de [ChartDataLabel](../chartdatalabel/) en esta colección. |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente de las etiquetas de datos de toda la serie. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y de línea de las etiquetas de datos. |
| [get_NumberFormat](./get_numberformat/)() | Obtiene una instancia de [ChartNumberFormat](../chartnumberformat/) que permite establecer el formato numérico para las etiquetas de datos de toda la serie. |
| [get_Orientation](./get_orientation/)() | Obtiene o establece la orientación del texto de las etiquetas de datos de toda la serie. |
| [get_Position](./get_position/)() | Obtiene o establece la posición de las etiquetas de datos. |
| [get_Rotation](./get_rotation/)() | Obtiene o establece la rotación de las etiquetas de datos de toda la serie en grados. |
| [get_Separator](./get_separator/)() | Obtiene o establece el separador de cadena utilizado para las etiquetas de datos de toda la serie. El valor predeterminado es una coma, excepto en los gráficos de pastel que muestran solo el nombre de la categoría y el porcentaje, donde se debe usar un salto de línea. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Permite especificar si se debe mostrar el tamaño de la burbuja en las etiquetas de datos de toda la serie. Se aplica solo a los gráficos de burbujas. El valor predeterminado es **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Permite especificar si se debe mostrar el nombre de la categoría en las etiquetas de datos de toda la serie. El valor predeterminado es **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Permite especificar si se deben mostrar los valores del rango de etiquetas de datos en las etiquetas de datos de toda la serie. El valor predeterminado es **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Permite especificar si se deben mostrar líneas guía de etiquetas de datos para las etiquetas de datos de toda la serie. El valor predeterminado es **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Permite especificar si se debe mostrar la clave de leyenda en las etiquetas de datos de toda la serie. El valor predeterminado es **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Permite especificar si se debe mostrar el valor de porcentaje en las etiquetas de datos de toda la serie. El valor predeterminado es **false**. Se aplica solo a los gráficos de pastel. |
| [get_ShowSeriesName](./get_showseriesname/)() | Devuelve o establece un Booleano para indicar el comportamiento de visualización del nombre de la serie en las etiquetas de datos de toda la serie. **true** para mostrar el nombre de la serie; **false** para ocultarlo. Por defecto **false**. |
| [get_ShowValue](./get_showvalue/)() | Permite especificar si se deben mostrar los valores en las etiquetas de datos de toda la serie. El valor predeterminado es **false**. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve [ChartDataLabel](../chartdatalabel/) para el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Permite especificar si se deben mostrar los valores del rango de etiquetas de datos en las etiquetas de datos de toda la serie. El valor predeterminado es **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Establecedor de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
