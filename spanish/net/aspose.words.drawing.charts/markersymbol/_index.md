---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words para .NET
description: Explore la enumeración Aspose.Words.Drawing.Charts.MarkerSymbol para obtener estilos de marcadores personalizables que mejoran las imágenes de sus gráficos y la presentación de datos.
type: docs
weight: 1240
url: /es/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Especifica el estilo del símbolo del marcador.

```csharp
public enum MarkerSymbol
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | `0` | Especifica que se dibujará un símbolo de marcador predeterminado en cada punto de datos. |
| Circle | `1` | Especifica que se dibujará un círculo en cada punto de datos. |
| Dash | `2` | Especifica que se dibujará un guion en cada punto de datos. |
| Diamond | `3` | Especifica que se dibujará un diamante en cada punto de datos. |
| Dot | `4` | Especifica que se dibujará un punto en cada punto de datos. |
| None | `5` | Especifica que no se dibujará nada en cada punto de datos. |
| Picture | `6` | Especifica que se dibujará una imagen en cada punto de datos. |
| Plus | `7` | Especifica que se dibujará un signo más en cada punto de datos. |
| Square | `8` | Especifica que se dibujará un cuadrado en cada punto de datos. |
| Star | `9` | Especifica que se dibujará una estrella en cada punto de datos. |
| Triangle | `10` | Especifica que se dibujará un triángulo en cada punto de datos. |
| X | `11` | Especifica que se dibujará una X en cada punto de datos. |

## Ejemplos

Muestra cómo trabajar con puntos de datos en un gráfico de líneas.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Enfatiza los puntos de datos del gráfico haciéndolos aparecer como formas de diamante.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Suaviza la línea que representa la primera serie de datos.
    chart.Series[0].Smooth = true;

    // Verifique que los puntos de datos de la primera serie no inviertan sus colores si el valor es negativo.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Para un gráfico más limpio, podemos borrar el formato individualmente.
    dataPoint.ClearFormat();

    // También podemos eliminar una serie entera de puntos de datos a la vez.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Aplica una cantidad de puntos de datos a una serie.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
