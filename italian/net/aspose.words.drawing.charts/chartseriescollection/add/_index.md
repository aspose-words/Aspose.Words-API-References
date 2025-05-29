---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words per .NET
description: Migliora i tuoi grafici senza sforzo con il metodo ChartSeriesCollection Add. Aggiungi senza problemi nuove serie a grafici a barre, istogrammi, linee e superfici per ottenere visualizzazioni dinamiche.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

Aggiunge nuovo[`ChartSeries`](../../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico a barre, a colonne, a linee e a superficie.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Valore di ritorno

Aggiunto di recente[`ChartSeries`](../../chartseries/) oggetto.

## Esempi

Mostra come creare un grafico di Pareto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico di Pareto.
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi una serie.
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

Mostra come creare un grafico a imbuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a imbuto.
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi una serie.
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

// Mostra le etichette dei dati.
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

Mostra come creare un grafico a scatola e baffi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a scatola e baffi.
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi una serie.
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

// Mostra le etichette dei dati.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

Mostra come creare un tipo appropriato di serie di grafici per un tipo di grafico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Esistono diversi modi per popolare la raccolta di serie di un grafico.
    // Diversi schemi di serie sono pensati per diversi tipi di grafici.
    // 1 - Grafico a colonne con colonne raggruppate e disposte lungo l'asse X per categoria:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserire due serie di valori decimali contenenti un valore per ciascuna rispettiva categoria.
    // Questo grafico a colonne avrà tre gruppi, ciascuno con due colonne.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Le categorie sono distribuite lungo l'asse X e i valori sono distribuiti lungo l'asse Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Grafico ad area con date distribuite lungo l'asse X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Inserire una serie con un valore decimale per ogni rispettiva data.
    // Le date saranno distribuite lungo un asse X lineare,
    // e i valori aggiunti a questa serie creeranno punti dati.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagramma di dispersione 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Ogni serie necessiterà di due array decimali di uguale lunghezza.
    // Il primo array contiene i valori X e il secondo contiene i corrispondenti valori Y
    // dei punti dati sul grafico del grafico.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Grafico a bolle:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Ogni serie necessiterà di tre array decimali di uguale lunghezza.
    // Il primo array contiene i valori X, il secondo contiene i corrispondenti valori Y,
    // e il terzo contiene i diametri per ciascuno dei punti dati del grafico.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserire un grafico utilizzando un generatore di documenti con un ChartType, larghezza e altezza specificati e rimuovere i relativi dati demo.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Guarda anche

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

Aggiunge nuovo[`ChartSeries`](../../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico a dispersione.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Valore di ritorno

Aggiunto di recente[`ChartSeries`](../../chartseries/) oggetto.

## Esempi

Mostra come creare un tipo appropriato di serie di grafici per un tipo di grafico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Esistono diversi modi per popolare la raccolta di serie di un grafico.
    // Diversi schemi di serie sono pensati per diversi tipi di grafici.
    // 1 - Grafico a colonne con colonne raggruppate e disposte lungo l'asse X per categoria:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserire due serie di valori decimali contenenti un valore per ciascuna rispettiva categoria.
    // Questo grafico a colonne avrà tre gruppi, ciascuno con due colonne.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Le categorie sono distribuite lungo l'asse X e i valori sono distribuiti lungo l'asse Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Grafico ad area con date distribuite lungo l'asse X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Inserire una serie con un valore decimale per ogni rispettiva data.
    // Le date saranno distribuite lungo un asse X lineare,
    // e i valori aggiunti a questa serie creeranno punti dati.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagramma di dispersione 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Ogni serie necessiterà di due array decimali di uguale lunghezza.
    // Il primo array contiene i valori X e il secondo contiene i corrispondenti valori Y
    // dei punti dati sul grafico del grafico.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Grafico a bolle:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Ogni serie necessiterà di tre array decimali di uguale lunghezza.
    // Il primo array contiene i valori X, il secondo contiene i corrispondenti valori Y,
    // e il terzo contiene i diametri per ciascuno dei punti dati del grafico.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserire un grafico utilizzando un generatore di documenti con un ChartType, larghezza e altezza specificati e rimuovere i relativi dati demo.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Guarda anche

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

Aggiunge nuovo[`ChartSeries`](../../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico Area, Radar e Azionario.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

## Esempi

Mostra come creare un tipo appropriato di serie di grafici per un tipo di grafico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Esistono diversi modi per popolare la raccolta di serie di un grafico.
    // Diversi schemi di serie sono pensati per diversi tipi di grafici.
    // 1 - Grafico a colonne con colonne raggruppate e disposte lungo l'asse X per categoria:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserire due serie di valori decimali contenenti un valore per ciascuna rispettiva categoria.
    // Questo grafico a colonne avrà tre gruppi, ciascuno con due colonne.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Le categorie sono distribuite lungo l'asse X e i valori sono distribuiti lungo l'asse Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Grafico ad area con date distribuite lungo l'asse X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Inserire una serie con un valore decimale per ogni rispettiva data.
    // Le date saranno distribuite lungo un asse X lineare,
    // e i valori aggiunti a questa serie creeranno punti dati.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagramma di dispersione 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Ogni serie necessiterà di due array decimali di uguale lunghezza.
    // Il primo array contiene i valori X e il secondo contiene i corrispondenti valori Y
    // dei punti dati sul grafico del grafico.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Grafico a bolle:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Ogni serie necessiterà di tre array decimali di uguale lunghezza.
    // Il primo array contiene i valori X, il secondo contiene i corrispondenti valori Y,
    // e il terzo contiene i diametri per ciascuno dei punti dati del grafico.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserire un grafico utilizzando un generatore di documenti con un ChartType, larghezza e altezza specificati e rimuovere i relativi dati demo.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Guarda anche

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

Aggiunge nuovo[`ChartSeries`](../../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico a bolle.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Valore di ritorno

Aggiunto di recente[`ChartSeries`](../../chartseries/) oggetto.

## Esempi

Mostra come creare un tipo appropriato di serie di grafici per un tipo di grafico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Esistono diversi modi per popolare la raccolta di serie di un grafico.
    // Diversi schemi di serie sono pensati per diversi tipi di grafici.
    // 1 - Grafico a colonne con colonne raggruppate e disposte lungo l'asse X per categoria:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserire due serie di valori decimali contenenti un valore per ciascuna rispettiva categoria.
    // Questo grafico a colonne avrà tre gruppi, ciascuno con due colonne.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Le categorie sono distribuite lungo l'asse X e i valori sono distribuiti lungo l'asse Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Grafico ad area con date distribuite lungo l'asse X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Inserire una serie con un valore decimale per ogni rispettiva data.
    // Le date saranno distribuite lungo un asse X lineare,
    // e i valori aggiunti a questa serie creeranno punti dati.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagramma di dispersione 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Ogni serie necessiterà di due array decimali di uguale lunghezza.
    // Il primo array contiene i valori X e il secondo contiene i corrispondenti valori Y
    // dei punti dati sul grafico del grafico.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Grafico a bolle:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Ogni serie necessiterà di tre array decimali di uguale lunghezza.
    // Il primo array contiene i valori X, il secondo contiene i corrispondenti valori Y,
    // e il terzo contiene i diametri per ciascuno dei punti dati del grafico.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserire un grafico utilizzando un generatore di documenti con un ChartType, larghezza e altezza specificati e rimuovere i relativi dati demo.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Guarda anche

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

Aggiunge nuovo[`ChartSeries`](../../chartseries/) questa raccolta. Utilizza questo metodo per aggiungere serie che hanno categorie di dati multilivello.

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### Valore di ritorno

Aggiunto di recente[`ChartSeries`](../../chartseries/) oggetto.

## Esempi

Mostra come creare un grafico a raggiera.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico Sunburst.
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi una serie.
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

// Mostra le etichette dei dati.
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

Mostra come creare un grafico ad albero.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico Treemap.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi una serie.
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

// Mostra le etichette dei dati.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Guarda anche

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

Aggiunge nuovo[`ChartSeries`](../../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie ai grafici istogramma.

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### Valore di ritorno

Aggiunto di recente[`ChartSeries`](../../chartseries/) oggetto.

## Osservazioni

Per tipi di grafico diversi da Istogramma, questo metodo aggiunge una serie con valori Y vuoti.

## Esempi

Mostra come creare un grafico a istogramma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a istogramma.
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi una serie.
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

### Guarda anche

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

Aggiunge nuovo[`ChartSeries`](../../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie ai grafici a cascata.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| seriesName | String | Nome della serie da aggiungere. |
| categories | String[] | Nomi delle categorie per l'asse X. |
| values | Double[] | Valori sull'asse Y. |
| isSubtotal | Boolean[] | Valori che indicano se il valore Y corrispondente è un subtotale. |

### Valore di ritorno

Aggiunto di recente[`ChartSeries`](../../chartseries/) oggetto.

## Osservazioni

Per tipi di grafico diversi da Waterfall,*isSubtotal* i valori vengono ignorati.

## Esempi

Mostra come creare un grafico a cascata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a cascata.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi una serie.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// Mostra le etichette dei dati.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### Guarda anche

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
