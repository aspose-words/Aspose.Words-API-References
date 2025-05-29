---
title: IChartDataPoint Interface
linktitle: IChartDataPoint
articleTitle: IChartDataPoint
second_title: Aspose.Words para .NET
description: Explora la interfaz Aspose.Words.Drawing.Charts.IChartDataPoint para obtener propiedades detalladas de los puntos de datos de los gráficos. ¡Mejora tu visualización de datos fácilmente!
type: docs
weight: 1220
url: /es/net/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface

Contiene propiedades de un solo punto de datos en el gráfico.

```csharp
public interface IChartDataPoint
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/ichartdatapoint/bubble3d/) { get; set; } | Especifica si se debe aplicar un efecto 3D a las burbujas del gráfico de burbujas. |
| [Explosion](../../aspose.words.drawing.charts/ichartdatapoint/explosion/) { get; set; } | Especifica la cantidad en que se moverá el punto de datos desde el centro del gráfico circular. Puede ser negativo; negativo significa que la propiedad no está configurada y no se debe aplicar ninguna explosión. Se aplica solo a gráficos circulares. |
| [InvertIfNegative](../../aspose.words.drawing.charts/ichartdatapoint/invertifnegative/) { get; set; } | Especifica si el elemento padre debe invertir sus colores si el valor es negativo. |
| [Marker](../../aspose.words.drawing.charts/ichartdatapoint/marker/) { get; } | Especifica un marcador de datos. El marcador se crea automáticamente cuando se solicita. |

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
