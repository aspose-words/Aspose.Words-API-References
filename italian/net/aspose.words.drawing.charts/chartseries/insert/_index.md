---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words per .NET
description: Migliora i tuoi grafici senza sforzo con il metodo ChartSeries Insert. Inserisci valori X in qualsiasi indice, ottimizzando la visualizzazione dei dati con facilità!
type: docs
weight: 200
url: /it/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

Inserisce il valore X specificato nella serie del grafico all'indice specificato. Se la serie supporta valori Y e dimensioni delle bolle, saranno vuoti per il valore X.

```csharp
public void Insert(int index, ChartXValue xValue)
```

## Osservazioni

Il punto dati corrispondente con la formattazione predefinita verrà inserito nella raccolta di punti dati. E, se vengono visualizzate le etichette dati, verrà inserita anche l'etichetta dati corrispondente con la formattazione predefinita.

## Esempi

Mostra come inserire dati in una serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();
// Popola la serie con i dati.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

Inserisce i valori X e Y specificati nella serie del grafico all'indice specificato.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## Osservazioni

Il punto dati corrispondente con la formattazione predefinita verrà inserito nella raccolta di punti dati. E, se vengono visualizzate le etichette dati, verrà inserita anche l'etichetta dati corrispondente con la formattazione predefinita.

## Esempi

Mostra come inserire dati in una serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();
// Popola la serie con i dati.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

Inserisce il valore X, il valore Y e la dimensione della bolla specificati nella serie del grafico all'indice specificato.

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## Osservazioni

Il punto dati corrispondente con la formattazione predefinita verrà inserito nella raccolta di punti dati. E, se vengono visualizzate le etichette dati, verrà inserita anche l'etichetta dati corrispondente con la formattazione predefinita.

## Esempi

Mostra come inserire dati in una serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Cancella i valori X e Y della prima serie.
series1.ClearValues();
// Popola la serie con i dati.
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Guarda anche

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
