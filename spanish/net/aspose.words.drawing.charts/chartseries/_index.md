---
title: Class ChartSeries
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartSeries clase. Representa las propiedades de la serie de gráficos.
type: docs
weight: 730
url: /es/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Representa las propiedades de la serie de gráficos.

```csharp
public class ChartSeries : IChartDataPoint
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } |  |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Especifica la configuración de las etiquetas de datos para toda la serie. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Devuelve una colección de objetos de formato para todos los puntos de datos de esta serie. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Proporciona acceso al formato de relleno y línea de la serie. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Obtiene o establece un indicador que indica si se muestran etiquetas de datos para la serie. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } |  |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Obtiene una entrada de leyenda para esta serie de gráfico. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } |  |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Obtiene o establece el nombre de la serie, si el nombre no se establece explícitamente, se genera utilizando index. De forma predeterminada, devuelve Serie más un índice basado. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Permite especificar si la línea que conecta los puntos del gráfico se suavizará mediante splines de Catmull-Rom. |

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

* interface [IChartDataPoint](../ichartdatapoint/)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)


