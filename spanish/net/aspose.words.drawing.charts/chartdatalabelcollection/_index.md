---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.ChartDataLabelCollection para gestionar eficientemente las etiquetas de datos de gráficos. ¡Mejore el aspecto visual de su documento hoy mismo!
type: docs
weight: 940
url: /es/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Representa una colección de[`ChartDataLabel`](../chartdatalabel/) .

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Devuelve el número de[`ChartDataLabel`](../chartdatalabel/) en esta colección. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Proporciona acceso al formato de fuente de las etiquetas de datos de toda la serie. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Proporciona acceso para rellenar y formatear las líneas de las etiquetas de datos. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Devuelve[`ChartDataLabel`](../chartdatalabel/) para el índice especificado. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Obtiene un[`ChartNumberFormat`](../chartnumberformat/) instancia que permite establecer el formato de número para las etiquetas de datos de toda la serie . |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabelcollection/orientation/) { get; set; } | Obtiene o establece la orientación del texto de las etiquetas de datos de toda la serie. |
| [Position](../../aspose.words.drawing.charts/chartdatalabelcollection/position/) { get; set; } | Obtiene o establece la posición de las etiquetas de datos. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabelcollection/rotation/) { get; set; } | Obtiene o establece la rotación de las etiquetas de datos de toda la serie en grados. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Obtiene o establece el separador de cadena utilizado para las etiquetas de datos de toda la serie. El valor predeterminado es una coma, excepto para los gráficos circulares que muestran solo el nombre de la categoría y el porcentaje, en cuyo caso se debe utilizar un salto de línea en su lugar. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Permite especificar si se mostrará el tamaño de la burbuja para las etiquetas de datos de toda la serie. Se aplica solo a los gráficos de burbujas. El valor predeterminado es`FALSO` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Permite especificar si se debe mostrar el nombre de la categoría para las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Permite especificar si los valores del rango de etiquetas de datos se mostrarán en las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Permite especificar si se deben mostrar las líneas guía de las etiquetas de datos para las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Permite especificar si se mostrará la clave de leyenda para las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Permite especificar si se mostrará el valor porcentual para las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` . Se aplica solo a gráficos circulares. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Devuelve o establece un valor booleano para indicar el comportamiento de visualización del nombre de la serie para las etiquetas de datos de toda la serie. `verdadero` para mostrar el nombre de la serie;`FALSO` para ocultar. Por defecto`FALSO` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Permite especificar si se mostrarán valores en las etiquetas de datos de toda la serie. El valor predeterminado es`FALSO` . |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Borra el formato de todos[`ChartDataLabel`](../chartdatalabel/) en esta colección. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Devuelve un objeto enumerador. |

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

* class [ChartDataLabel](../chartdatalabel/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
