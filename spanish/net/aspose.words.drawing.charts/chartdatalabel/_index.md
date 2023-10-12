---
title: Class ChartDataLabel
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabel clase. Representa la etiqueta de datos en un punto del gráfico o línea de tendencia.
type: docs
weight: 670
url: /es/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Representa la etiqueta de datos en un punto del gráfico o línea de tendencia.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) artículo de documentación.

```csharp
public class ChartDataLabel
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Proporciona acceso al formato de fuente de esta etiqueta de datos. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Proporciona acceso al formato de relleno y línea de la etiqueta de datos. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Especifica el índice del elemento contenedor. Este índice determinará a cuál de las colecciones secundarias de los padres se aplica este elemento. El valor predeterminado es 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Obtiene/establece un indicador que indica si esta etiqueta está oculta. El valor predeterminado es`FALSO` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Devoluciones`verdadero` si esta etiqueta de datos tiene algo que mostrar. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Devuelve el formato numérico del elemento principal. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Obtiene o establece el separador de cadena utilizado para las etiquetas de datos en un gráfico. El valor predeterminado es una coma, excepto en los gráficos circulares que muestran solo el nombre de la categoría y el porcentaje, cuando en su lugar se utilizará un salto de línea . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Permite especificar si se mostrará el tamaño de la burbuja para las etiquetas de datos en un gráfico. Se aplica solo a gráficos de burbujas. El valor predeterminado es`FALSO` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Permite especificar si el nombre de la categoría se mostrará para las etiquetas de datos en un gráfico. El valor predeterminado es`FALSO` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Permite especificar si los valores de las etiquetas de datos se mostrarán en las etiquetas de datos. El valor predeterminado es`FALSO` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Permite especificar si es necesario mostrar las líneas guía de la etiqueta de datos. El valor predeterminado es`FALSO` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Permite especificar si se mostrará la clave de leyenda para las etiquetas de datos en un gráfico. El valor predeterminado es`FALSO` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Permite especificar si se mostrará el valor porcentual para las etiquetas de datos en un gráfico. El valor predeterminado es`FALSO` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Devuelve o establece un valor booleano para indicar el comportamiento de visualización del nombre de la serie para las etiquetas de datos en un gráfico. `verdadero` para mostrar el nombre de la serie;`FALSO` esconder. Por defecto`FALSO` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Permite especificar si se mostrarán valores en las etiquetas de datos. El valor predeterminado es`FALSO` . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Borra el formato de esta etiqueta de datos. Las propiedades se establecen en los valores predeterminados definidos en la colección principal de etiquetas data . |

### Observaciones

En una serie, el`ChartDataLabel` El objeto es miembro del[`ChartDataLabelCollection`](../chartdatalabelcollection/) . El[`ChartDataLabelCollection`](../chartdatalabelcollection/) contiene una`ChartDataLabel` objeto para cada punto.

### Ejemplos

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
    // Estas etiquetas aparecerán junto a cada punto de datos en el gráfico y mostrarán su valor.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Cambia la cadena separadora para cada etiqueta de datos de una serie.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // Para obtener un gráfico más limpio, podemos eliminar las etiquetas de datos individualmente.
    chart.Series[1].DataLabels[2].ClearFormat();

    // También podemos eliminar una serie completa de sus etiquetas de datos a la vez.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Aplique etiquetas de datos con formato de número personalizado y separador a varios puntos de datos en una serie.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series.HasDataLabels = true;

        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        series.DataLabels[i].IsHidden = false;
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


