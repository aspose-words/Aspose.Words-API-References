---
title: ChartDataLabelCollection.ShowSeriesName
second_title: Aspose.Words per .NET API Reference
description: ChartDataLabelCollection proprietà. Restituisce o imposta un valore booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dellintera serie. VERO per mostrare il nome della seriefalso nascondere. Per impostazione predefinitafalso .
type: docs
weight: 130
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

Restituisce o imposta un valore booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. `VERO` per mostrare il nome della serie;`falso` nascondere. Per impostazione predefinita`falso` .

```csharp
public bool ShowSeriesName { get; set; }
```

### Osservazioni

Il valore definito per questa proprietà può essere sovrascritto per una singola etichetta dati utilizzando [`ShowSeriesName`](../../chartdatalabel/showseriesname/) proprietà.

### Esempi

Mostra come utilizzare le etichette dati di un grafico a bolle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Cancella le serie di dati dimostrativi del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Aggiungi una serie personalizzata con le coordinate X/Y e il diametro di ciascuna bolla.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Abilita le etichette dati e quindi modifica il loro aspetto.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

### Guarda anche

* class [ChartDataLabelCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* assemblea [Aspose.Words](../../../)


