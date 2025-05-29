---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: Mejore sus gráficos fácilmente con el método ChartSeriesCollection Add. Añada nuevas series fácilmente a gráficos de barras, columnas, líneas y superficies para obtener imágenes dinámicas.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

Agrega nuevo[`ChartSeries`](../../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráficos de barras, columnas, líneas y superficies.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Valor_devuelto

Recientemente añadido[`ChartSeries`](../../chartseries/) objeto.

## Ejemplos

Muestra cómo crear un diagrama de Pareto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un diagrama de Pareto.
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

Muestra cómo crear un gráfico de embudo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de embudo.
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

Muestra cómo crear un gráfico de caja y bigotes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de caja y bigotes.
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
ChartSeries series = chart.Series.Add(
    "Points by Years",
    new string[]
    {
        "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC",
        "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR",
        "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA"
    },
    new double[]
    {
        91, 80, 100, 77, 90, 104, 105, 118, 120, 101,
        114, 107, 110, 60, 79, 78, 77, 102, 101, 113,
        94, 93, 84, 71, 80, 103, 80, 94, 100, 101
    });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

Agrega nuevo[`ChartSeries`](../../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráfico de dispersión.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Valor_devuelto

Recientemente añadido[`ChartSeries`](../../chartseries/) objeto.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

Agrega nuevo[`ChartSeries`](../../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráficos de área, radar y acciones.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

Agrega nuevo[`ChartSeries`](../../chartseries/) a esta colección. Utilice este método para agregar series a cualquier tipo de gráfico de burbujas.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Valor_devuelto

Recientemente añadido[`ChartSeries`](../../chartseries/) objeto.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

Agrega nuevo[`ChartSeries`](../../chartseries/) esta colección. Utilice este método para agregar series que tengan categorías de datos de varios niveles.

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### Valor_devuelto

Recientemente añadido[`ChartSeries`](../../chartseries/) objeto.

## Ejemplos

Muestra cómo crear un gráfico de rayos de sol.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico Sunburst.
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
ChartSeries series = chart.Series.Add(
    "Sales",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Sales - Europe", "UK", "London Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Liverpool Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Manchester Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Paris Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Lyon Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Denver Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Seattle Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Detroit Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Houston Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Toronto Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Montreal Dep."),
        new ChartMultilevelValue("Sales - Oceania", "Australia", "Sydney Dep."),
        new ChartMultilevelValue("Sales - Oceania", "New Zealand", "Auckland Dep.")
    },
    new double[] { 1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694 });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

Muestra cómo crear un gráfico de mapa de árbol.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de mapa de árbol.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Ver también

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

Agrega nuevo[`ChartSeries`](../../chartseries/) a esta colección. Utilice este método para agregar series a los gráficos de histograma.

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### Valor_devuelto

Recientemente añadido[`ChartSeries`](../../chartseries/) objeto.

## Observaciones

Para tipos de gráficos distintos de Histograma, este método agrega una serie con valores Y vacíos.

## Ejemplos

Muestra cómo crear un gráfico de histograma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de histograma.
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
chart.Series.Add(
    "Avg Temperature",
    new double[]
    {
        51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4,
        53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7,
        56.3, 55.9, 55.6
    });

doc.Save(ArtifactsDir + "Charts.Histogram.docx");
```

### Ver también

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

Agrega nuevo[`ChartSeries`](../../chartseries/) a esta colección. Utilice este método para agregar series a los gráficos de cascada.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| seriesName | String | Se agregará un nombre a la serie. |
| categories | String[] | Nombres de categorías para el eje X. |
| values | Double[] | Valores del eje Y. |
| isSubtotal | Boolean[] | Valores que indican si el valor Y correspondiente es un subtotal. |

### Valor_devuelto

Recientemente añadido[`ChartSeries`](../../chartseries/) objeto.

## Observaciones

Para tipos de gráficos distintos de Cascada,*isSubtotal* Los valores se ignoran.

## Ejemplos

Muestra cómo crear un gráfico de cascada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de cascada.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

//Eliminar serie generada por defecto.
chart.Series.Clear();

//Añadir una serie.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// Mostrar etiquetas de datos.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### Ver también

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
