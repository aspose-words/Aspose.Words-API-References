---
title: ChartType Enum
linktitle: ChartType
articleTitle: ChartType
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.ChartType enumeración. Especifica el tipo de gráfico en C#.
type: docs
weight: 830
url: /es/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Especifica el tipo de gráfico.

```csharp
public enum ChartType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Area | `0` | Gráfico de áreas. |
| AreaStacked | `1` | Gráfico de áreas apiladas. |
| AreaPercentStacked | `2` | Gráfico de áreas apiladas al 100 %. |
| Area3D | `3` | Gráfico de áreas 3D. |
| Area3DStacked | `4` | Gráfico de áreas apiladas 3D. |
| Area3DPercentStacked | `5` | Gráfico 3D de áreas apiladas 100%. |
| Bar | `6` | Gráfico de barras. |
| BarStacked | `7` | Gráfico de barras apiladas. |
| BarPercentStacked | `8` | Gráfico de barras apiladas 100 %. |
| Bar3D | `9` | Gráfico de barras 3D. |
| Bar3DStacked | `10` | Gráfico de barras apiladas 3D. |
| Bar3DPercentStacked | `11` | Gráfico de barras 3D 100% apiladas. |
| Bubble | `12` | Gráfico de burbujas. |
| Bubble3D | `13` | Gráfico de burbujas 3D. |
| Column | `14` | Gráfico de columnas. |
| ColumnStacked | `15` | Gráfico de columnas apiladas. |
| ColumnPercentStacked | `16` | Gráfico de columnas 100% apiladas. |
| Column3D | `17` | Gráfico de columnas 3D. |
| Column3DStacked | `18` | Gráfico de columnas apiladas 3D. |
| Column3DPercentStacked | `19` | Gráfico de columnas 3D 100% apiladas. |
| Column3DClustered | `20` | Gráfico de columnas agrupadas en 3D. |
| Doughnut | `21` | Gráfico de anillos. |
| Line | `22` | Gráfico de líneas. |
| LineStacked | `23` | Gráfico de líneas apiladas. |
| LinePercentStacked | `24` | Gráfico de líneas apiladas 100%. |
| Line3D | `25` | Gráfico de líneas 3D. |
| Pie | `26` | Gráfico circular. |
| Pie3D | `27` | Gráfico circular 3D. |
| PieOfBar | `28` | Gráfico circular de barras. |
| PieOfPie | `29` | Gráfico circular. |
| Radar | `30` | Gráfico radar. |
| Scatter | `31` | Gráfico de dispersión. |
| Stock | `32` | Gráfico de cotizaciones. |
| Surface | `33` | Gráfico de superficie. |
| Surface3D | `34` | Gráfico de superficie 3D. |

## Ejemplos

Muestra cómo crear un tipo apropiado de serie de gráficos para un tipo de gráfico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Hay varias formas de completar la colección de series de un gráfico.
    // Los diferentes esquemas de series están destinados a diferentes tipos de gráficos.
    // 1 - Gráfico de columnas con columnas agrupadas y agrupadas a lo largo del eje X por categoría:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserta dos series de valores decimales que contengan un valor para cada categoría respectiva.
    // Este gráfico de columnas tendrá tres grupos, cada uno con dos columnas.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

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

    // Insertar una serie con un valor decimal para cada fecha respectiva.
    // Las fechas se distribuirán a lo largo de un eje X lineal,
    // y los valores agregados a esta serie crearán puntos de datos.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagrama de dispersión 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Cada serie necesitará dos matrices decimales de igual longitud.
    // La primera matriz contiene valores X y la segunda contiene los valores Y correspondientes
    // de puntos de datos en el gráfico del cuadro.
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

    // Cada serie necesitará tres matrices decimales de igual longitud.
    // La primera matriz contiene valores X, la segunda contiene los valores Y correspondientes,
    // y el tercero contiene diámetros para cada uno de los puntos de datos del gráfico.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserte un gráfico utilizando un generador de documentos de un tipo de gráfico, ancho y alto específicos, y elimine sus datos de demostración.
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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
