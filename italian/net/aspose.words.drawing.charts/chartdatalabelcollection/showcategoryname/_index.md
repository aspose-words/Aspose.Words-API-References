---
title: ChartDataLabelCollection.ShowCategoryName
linktitle: ShowCategoryName
articleTitle: ShowCategoryName
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShowCategoryName in ChartDataLabelCollection. Controlla la visibilità delle etichette dati per le tue serie e migliora la chiarezza del tuo grafico!
type: docs
weight: 110
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dati dell'intera serie. Il valore predefinito è`falso` .

```csharp
public bool ShowCategoryName { get; set; }
```

## Osservazioni

Il valore definito per questa proprietà può essere sovrascritto per una singola etichetta dati utilizzando [`ShowCategoryName`](../../chartdatalabel/showcategoryname/) proprietà.

## Esempi

Mostra come lavorare con le etichette dati di un grafico a bolle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

 // Aggiungi una serie personalizzata con coordinate X/Y e diametro di ciascuna delle bolle.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Abilita le etichette dati e quindi modificane l'aspetto.
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
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
