---
title: ChartAxis.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxis Type para identificar fácilmente los tipos de ejes y mejorar la visualización de sus datos para obtener información más clara y un mejor análisis.
type: docs
weight: 260
url: /es/net/aspose.words.drawing.charts/chartaxis/type/
---
## ChartAxis.Type property

Devuelve el tipo del eje.

```csharp
public ChartAxisType Type { get; }
```

## Ejemplos

Muestra cómo crear un tipo de serie de gráficos apropiado para un tipo de gráfico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Hay varias formas de completar la colección de series de un gráfico.
    // Diferentes esquemas de series están pensados para distintos tipos de gráficos.
    // 1 - Gráfico de columnas con columnas agrupadas y en bandas a lo largo del eje X por categoría:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserte dos series de valores decimales que contengan un valor para cada categoría respectiva.
    //Este gráfico de columnas tendrá tres grupos, cada uno con dos columnas.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Las categorías se distribuyen a lo largo del eje X y los valores se distribuyen a lo largo del eje Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Gráfico de áreas con fechas distribuidas a lo largo del eje X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Inserta una serie con un valor decimal para cada fecha respectiva.
    //Las fechas se distribuirán a lo largo de un eje X lineal,
    // y los valores agregados a esta serie crearán puntos de datos.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagrama de dispersión 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    //Cada serie necesitará dos matrices decimales de igual longitud.
    // La primera matriz contiene valores X y la segunda contiene valores Y correspondientes
    // de puntos de datos en el gráfico del gráfico.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Gráfico de burbujas:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    //Cada serie necesitará tres matrices decimales de igual longitud.
    // La primera matriz contiene valores X, la segunda contiene valores Y correspondientes,
    // y el tercero contiene los diámetros de cada uno de los puntos de datos del gráfico.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserte un gráfico utilizando un generador de documentos de un ChartType, ancho y alto específicos, y elimine sus datos de demostración.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Ver también

* enum [ChartAxisType](../../chartaxistype/)
* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
