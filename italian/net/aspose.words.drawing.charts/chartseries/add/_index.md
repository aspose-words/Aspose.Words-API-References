---
title: ChartSeries.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words per .NET
description: Scopri il metodo ChartSeries Add per integrare facilmente i valori X nei tuoi grafici. Migliora la visualizzazione dei dati con il supporto per i valori Y e le dimensioni delle bolle.
type: docs
weight: 160
url: /it/net/aspose.words.drawing.charts/chartseries/add/
---
## Add(*[ChartXValue](../../chartxvalue/)*) {#add}

Aggiunge il valore X specificato alla serie del grafico. Se la serie supporta valori Y e dimensioni delle bolle, saranno vuoti per il valore X.

```csharp
public void Add(ChartXValue xValue)
```

## Esempi

Mostra come popolare le serie di grafici con i dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();

// Popola la serie con i dati.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Cancella i valori X e Y della seconda serie.
series2.Clear();

// Popola la serie con i dati.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#add_1}

Aggiunge i valori X e Y specificati alla serie del grafico.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue)
```

## Esempi

Mostra come aggiungere/rimuovere valori dai dati del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries department1Series = chart.Series[0];
ChartSeries department2Series = chart.Series[1];

// Rimuove il primo valore in entrambe le serie.
department1Series.Remove(0);
department2Series.Remove(0);

// Aggiunge nuovi valori ad entrambe le serie.
ChartXValue newXCategory = ChartXValue.FromString("Q1, 2023");
department1Series.Add(newXCategory, ChartYValue.FromDouble(10.3));
department2Series.Add(newXCategory, ChartYValue.FromDouble(5.7));

doc.Save(ArtifactsDir + "Charts.ChartDataValues.docx");
```

Mostra come popolare le serie di grafici con i dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();

// Popola la serie con i dati.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Cancella i valori X e Y della seconda serie.
series2.Clear();

// Popola la serie con i dati.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Add(*[ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#add_2}

Aggiunge il valore X, il valore Y e la dimensione della bolla specificati alla serie del grafico.

```csharp
public void Add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Esempi

Mostra come popolare le serie di grafici con i dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();

// Popola la serie con i dati.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Cancella i valori X e Y della seconda serie.
series2.Clear();

// Popola la serie con i dati.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
