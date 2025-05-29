---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartDataLabel para una mejor visualización de datos en gráficos. ¡Mejore sus presentaciones con etiquetas de datos precisas!
type: docs
weight: 930
url: /es/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Representa la etiqueta de datos en un punto del gráfico o una línea de tendencia.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartDataLabel
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Proporciona acceso al formato de fuente de esta etiqueta de datos. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Proporciona acceso al relleno y formato de línea de la etiqueta de datos. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Especifica el índice del elemento contenedor. Este índice determinará a cuál de las colecciones de hijos del padre se aplica este elemento. El valor predeterminado es 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Obtiene/establece un indicador que indica si esta etiqueta está oculta. El valor predeterminado es`FALSO` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Devuelve`verdadero` Si esta etiqueta de datos tiene algo que mostrar. |
| [Left](../../aspose.words.drawing.charts/chartdatalabel/left/) { get; set; } | Obtiene o establece la distancia de la etiqueta de datos en puntos desde el borde izquierdo del gráfico o desde la posición especificada por su[`Position`](./position/) propiedad, dependiendo del valor de la misma[`LeftMode`](./leftmode/) propiedad. |
| [LeftMode](../../aspose.words.drawing.charts/chartdatalabel/leftmode/) { get; set; } | Obtiene o establece el modo de interpretación de la[`Left`](./left/) Valor de la propiedad: si establece la ubicación de la etiqueta de datos desde el borde izquierdo del gráfico o desde la posición especificada por su[`Position`](./position/) propiedad. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Devuelve el formato de número del elemento padre. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabel/orientation/) { get; set; } | Obtiene o establece la orientación del texto de la etiqueta. |
| [Position](../../aspose.words.drawing.charts/chartdatalabel/position/) { get; set; } | Obtiene o establece la posición de la etiqueta de datos. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabel/rotation/) { get; set; } | Obtiene o establece la rotación de la etiqueta en grados. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Obtiene o establece el separador de cadena utilizado para las etiquetas de datos en un gráfico. El valor predeterminado es una coma, excepto para los gráficos circulares que muestran solo el nombre de la categoría y el porcentaje, en cuyo caso se utilizará un salto de línea en su lugar. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Permite especificar si se mostrará el tamaño de la burbuja para las etiquetas de datos en un gráfico. Se aplica solo a gráficos de burbujas. El valor predeterminado es`FALSO` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Permite especificar si se mostrará el nombre de la categoría para las etiquetas de datos en un gráfico. El valor predeterminado es`FALSO` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Permite especificar si los valores del rango de etiquetas de datos se mostrarán en las etiquetas de datos. El valor predeterminado es`FALSO` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Permite especificar si se deben mostrar las líneas guía de la etiqueta de datos. El valor predeterminado es`FALSO` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Permite especificar si se mostrará la clave de leyenda para las etiquetas de datos en un gráfico. El valor predeterminado es`FALSO` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Permite especificar si se mostrará el valor porcentual para las etiquetas de datos en un gráfico. El valor predeterminado es`FALSO` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Devuelve o establece un valor booleano para indicar el comportamiento de visualización del nombre de la serie para las etiquetas de datos en un gráfico. `verdadero` para mostrar el nombre de la serie;`FALSO` para ocultar. Por defecto`FALSO` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Permite especificar si se mostrarán valores en las etiquetas de datos. El valor predeterminado es`FALSO` . |
| [Top](../../aspose.words.drawing.charts/chartdatalabel/top/) { get; set; } | Obtiene o establece la distancia de la etiqueta de datos en puntos desde el borde superior del gráfico o desde la posición especificada por su[`Position`](./position/) propiedad, dependiendo del valor de la misma[`TopMode`](./topmode/) propiedad. |
| [TopMode](../../aspose.words.drawing.charts/chartdatalabel/topmode/) { get; set; } | Obtiene o establece el modo de interpretación de la[`Top`](./top/) Valor de la propiedad: si establece la ubicación de la etiqueta de datos desde el borde superior del gráfico o desde la posición especificada por su[`Position`](./position/) propiedad. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Borra el formato de esta etiqueta de datos. Las propiedades se establecen en los valores predeterminados definidos en la colección de etiquetas principal data . |

## Observaciones

En una serie, el`ChartDataLabel` El objeto es un miembro de la[`ChartDataLabelCollection`](../chartdatalabelcollection/) . El[`ChartDataLabelCollection`](../chartdatalabelcollection/) contiene un`ChartDataLabel` objeto para cada punto.

## Ejemplos

Muestra cómo aplicar etiquetas a puntos de datos en un gráfico de líneas.

```csharp
public void DataLabels()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Aplicar etiquetas de datos a cada serie del gráfico.
    //Estas etiquetas aparecerán junto a cada punto de datos en el gráfico y mostrarán su valor.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Cambia la cadena separadora para cada etiqueta de datos en una serie.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // Para obtener un gráfico más limpio, podemos eliminar las etiquetas de datos individualmente.
    dataLabel.ClearFormat();

    // También podemos eliminar una serie entera de sus etiquetas de datos a la vez.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Aplicar etiquetas de datos con formato de número personalizado y separador a varios puntos de datos en una serie.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    series.HasDataLabels = true;
    series.Explosion = 40;

    for (int i = 0; i < labelsCount; i++)
    {
        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.False(series.DataLabels[i].IsHidden);
        Assert.False(series.DataLabels[i].ShowDataLabelsRange);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.False(series.DataLabels[i].ShowDataLabelsRange);
        Assert.True(series.DataLabels[i].IsVisible);
        Assert.False(series.DataLabels[i].IsHidden);
    }
}
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
