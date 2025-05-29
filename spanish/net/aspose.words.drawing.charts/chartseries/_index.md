---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.ChartSeries, su clave para mejorar las propiedades de las series de gráficos para la creación y visualización dinámica de documentos.
type: docs
weight: 1070
url: /es/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Representa las propiedades de la serie de gráficos.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class ChartSeries : IChartDataPoint
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Especifica si se debe aplicar un efecto 3D a las burbujas del gráfico de burbujas. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Obtiene una colección de tamaños de burbujas para esta serie de gráficos. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Especifica la configuración de las etiquetas de datos para toda la serie. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Devuelve una colección de objetos de formato para todos los puntos de datos de esta serie. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Especifica la cantidad en que se moverá el punto de datos desde el centro del gráfico circular. Puede ser negativo; negativo significa que la propiedad no está configurada y no se debe aplicar ninguna explosión. Se aplica solo a gráficos circulares. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Proporciona acceso al relleno y formato de línea de la serie. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Obtiene o establece un indicador que indica si se muestran las etiquetas de datos para la serie. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Especifica si el elemento padre debe invertir sus colores si el valor es negativo. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Obtiene una entrada de leyenda para esta serie de gráficos. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Especifica un marcador de datos. El marcador se crea automáticamente cuando se solicita. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Obtiene o establece el nombre de la serie, si el nombre no se establece explícitamente, se genera utilizando el índice. De manera predeterminada, devuelve Serie más uno basado en el índice. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Obtiene el tipo de esta serie de gráficos. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Permite especificar si la línea que conecta los puntos en el gráfico se suavizará utilizando splines Catmull-Rom. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Obtiene una colección de valores X para esta serie de gráficos. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Obtiene una colección de valores Y para esta serie de gráficos. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Agrega el valor X especificado a la serie del gráfico. Si la serie admite valores Y y tamaños de burbuja, estarán vacíos para el valor X. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Agrega los valores X e Y especificados a la serie del gráfico. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Agrega el valor X, el valor Y y el tamaño de burbuja especificados a la serie del gráfico. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Elimina todos los valores de datos de la serie gráfica. Se borra el formato de todos los puntos de datos y etiquetas de datos. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Elimina todos los valores de datos de la serie del gráfico conservando el formato de los puntos de datos y las etiquetas de datos. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | Copia el formato de punto de datos predeterminado del punto de datos con el índice especificado. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Inserta el valor X especificado en la serie del gráfico en el índice especificado. Si la serie admite valores Y y tamaños de burbuja, estarán vacíos para el valor X. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Inserta los valores X e Y especificados en la serie del gráfico en el índice especificado. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Inserta el valor X, el valor Y y el tamaño de burbuja especificados en la serie del gráfico en el índice especificado. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Elimina el valor X, el valor Y y el tamaño de burbuja, si es compatible, de la serie del gráfico en el índice especificado. También se eliminan el punto de datos y la etiqueta de datos correspondientes. |

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

* interface [IChartDataPoint](../ichartdatapoint/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
