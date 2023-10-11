---
title: ChartDataLabelCollection.ShowBubbleSize
second_title: Aspose.Words per .NET API Reference
description: ChartDataLabelCollection proprietà. Permette di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati dellintera serie. Si applica solo ai grafici a bolle. Il valore predefinito èfalso .
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/
---
## ChartDataLabelCollection.ShowBubbleSize property

Permette di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati dell'intera serie. Si applica solo ai grafici a bolle. Il valore predefinito è`falso` .

```csharp
public bool ShowBubbleSize { get; set; }
```

### Osservazioni

Il valore definito per questa proprietà può essere sovrascritto per una singola etichetta dati utilizzando [`ShowBubbleSize`](../../chartdatalabel/showbubblesize/) proprietà.

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


