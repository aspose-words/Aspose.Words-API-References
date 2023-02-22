---
title: Class ChartDataLabelCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection clase. Representa una colección deChartDataLabel .
type: docs
weight: 640
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Representa una colección de[`ChartDataLabel`](../chartdatalabel/) .

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Devuelve el número de[`ChartDataLabel`](../chartdatalabel/) en esta colección. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Devoluciones[`ChartDataLabel`](../chartdatalabel/) para el índice especificado. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Obtiene un[`ChartNumberFormat`](../chartnumberformat/) instancia que permite configurar el formato de número para las etiquetas de datos de la serie completa . |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Obtiene o establece el separador de cadenas utilizado para las etiquetas de datos de toda la serie. El valor predeterminado es una coma, excepto en los gráficos circulares que muestran solo el nombre de la categoría y el porcentaje, en los que se debe usar un salto de línea en su lugar. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Permite especificar si se mostrará el tamaño de la burbuja para las etiquetas de datos de toda la serie. Se aplica solo a gráficos de burbujas. El valor predeterminado es **falso** . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Permite especificar si se mostrará el nombre de la categoría para las etiquetas de datos de toda la serie. El valor predeterminado es **falso** . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Permite especificar si los valores del rango de etiquetas de datos se mostrarán en las etiquetas de datos de toda la serie. El valor predeterminado es **falso** . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Permite especificar si es necesario mostrar las líneas guía de las etiquetas de datos para las etiquetas de datos de toda la serie. El valor predeterminado es **falso** . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Permite especificar si se mostrará la clave de leyenda para las etiquetas de datos de toda la serie. El valor predeterminado es **falso** . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Permite especificar si se mostrará el valor porcentual para las etiquetas de datos de toda la serie. El valor predeterminado es **falso** . Se aplica solo a gráficos circulares. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Devuelve o establece un valor booleano para indicar el comportamiento de visualización del nombre de la serie para las etiquetas de datos de toda la serie.  **Verdadero**para mostrar el nombre de la serie. **Falso** esconder. Por defecto **falso** . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Permite especificar si los valores se mostrarán en las etiquetas de datos de toda la serie. El valor predeterminado es **falso** . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Borra el formato de todos[`ChartDataLabel`](../chartdatalabel/) en esta colección. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Devuelve un objeto enumerador. |

### Ejemplos

Muestra cómo aplicar etiquetas a puntos de datos en un gráfico de líneas.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Aplicar etiquetas de datos a cada serie en el gráfico.
    // Estas etiquetas aparecerán junto a cada punto de datos en el gráfico y mostrarán su valor.
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

    // Para un gráfico de aspecto más limpio, podemos eliminar las etiquetas de datos de forma individual.
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

* class [ChartDataLabel](../chartdatalabel/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)


