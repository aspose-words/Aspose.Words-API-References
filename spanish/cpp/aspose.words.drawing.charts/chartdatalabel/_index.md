---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel class"
linktitle: "ChartDataLabel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel class. Representa una etiqueta de datos en un punto de gráfico o línea de tendencia. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Representa la etiqueta de datos en un punto o línea de tendencia del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormat](./clearformat/)() | Borra el formato de esta etiqueta de datos. Las propiedades se establecen en los valores predeterminados definidos en la colección de etiquetas de datos principal. |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente de esta etiqueta de datos. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y línea de la etiqueta de datos. |
| [get_Index](./get_index/)() | Especifica el índice del elemento contenedor. Este índice determinará a cuál de las colecciones de hijos del padre se aplica este elemento. El valor predeterminado es 0. |
| [get_IsHidden](./get_ishidden/)() | Obtiene/establece una bandera que indica si esta etiqueta está oculta. El valor predeterminado es **false**. |
| [get_IsVisible](./get_isvisible/)() | Devuelve **true** si esta etiqueta de datos tiene algo que mostrar. |
| [get_Left](./get_left/)() | Obtiene o establece la distancia de la etiqueta de datos en puntos desde el borde izquierdo del gráfico o desde la posición especificada por su propiedad [Position](./get_position/), dependiendo del valor de la propiedad [LeftMode](./get_leftmode/). |
| [get_LeftMode](./get_leftmode/)() | Obtiene o establece el modo de interpretación del valor de la propiedad [Left](./get_left/): si establece la ubicación de la etiqueta de datos desde el borde izquierdo del gráfico o desde la posición especificada por su propiedad [Position](./get_position/). |
| [get_NumberFormat](./get_numberformat/)() | Devuelve el formato numérico del elemento padre. |
| [get_Orientation](./get_orientation/)() | Obtiene o establece la orientación del texto de la etiqueta. |
| [get_Position](./get_position/)() | Obtiene o establece la posición de la etiqueta de datos. |
| [get_Rotation](./get_rotation/)() | Obtiene o establece la rotación de la etiqueta en grados. |
| [get_Separator](./get_separator/)() | Obtiene el separador de cadena utilizado para las etiquetas de datos en un gráfico. El valor predeterminado es una coma, excepto en los gráficos de pastel que muestran solo el nombre de la categoría y el porcentaje, donde se debe usar un salto de línea. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Permite especificar si se debe mostrar el tamaño de la burbuja para las etiquetas de datos en un gráfico. Se aplica solo a los gráficos de burbujas. El valor predeterminado es **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Permite especificar si el nombre de la categoría se mostrará en las etiquetas de datos de un gráfico. El valor predeterminado es **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Permite especificar si los valores del rango de etiquetas de datos se mostrarán en las etiquetas de datos. El valor predeterminado es **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Permite especificar si se deben mostrar las líneas guía de la etiqueta de datos. El valor predeterminado es **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Permite especificar si la clave de la leyenda se mostrará en las etiquetas de datos de un gráfico. El valor predeterminado es **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Permite especificar si el valor de porcentaje se mostrará en las etiquetas de datos de un gráfico. El valor predeterminado es **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Devuelve un Booleano que indica el comportamiento de visualización del nombre de la serie en las etiquetas de datos de un gráfico. **true** para mostrar el nombre de la serie; **false** para ocultarlo. Por defecto **false**. |
| [get_ShowValue](./get_showvalue/)() | Permite especificar si los valores se mostrarán en las etiquetas de datos. El valor predeterminado es **false**. |
| [get_Top](./get_top/)() | Obtiene o establece la distancia de la etiqueta de datos en puntos desde el borde superior del gráfico o desde la posición especificada por su propiedad [Position](./get_position/), según el valor de la propiedad [TopMode](./get_topmode/). |
| [get_TopMode](./get_topmode/)() | Obtiene o establece el modo de interpretación del valor de la propiedad [Top](./get_top/): si establece la ubicación de la etiqueta de datos desde el borde superior del gráfico o desde la posición especificada por su propiedad [Position](./get_position/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Obtiene/establece una bandera que indica si esta etiqueta está oculta. El valor predeterminado es **false**. |
| [set_Left](./set_left/)(double) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Establece el separador de cadena utilizado para las etiquetas de datos en un gráfico. El valor predeterminado es una coma, excepto en los gráficos de pastel que muestran solo el nombre de la categoría y el porcentaje, donde se usará un salto de línea. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Permite especificar si el nombre de la categoría se mostrará en las etiquetas de datos de un gráfico. El valor predeterminado es **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Permite especificar si los valores del rango de etiquetas de datos se mostrarán en las etiquetas de datos. El valor predeterminado es **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Permite especificar si se deben mostrar las líneas guía de la etiqueta de datos. El valor predeterminado es **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Permite especificar si la clave de la leyenda se mostrará en las etiquetas de datos de un gráfico. El valor predeterminado es **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Permite especificar si el valor de porcentaje se mostrará en las etiquetas de datos de un gráfico. El valor predeterminado es **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Establece un Booleano que indica el comportamiento de visualización del nombre de la serie en las etiquetas de datos de un gráfico. **true** para mostrar el nombre de la serie; **false** para ocultarlo. Por defecto **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Permite especificar si los valores se mostrarán en las etiquetas de datos. El valor predeterminado es **false**. |
| [set_Top](./set_top/)(double) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Método set para [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
