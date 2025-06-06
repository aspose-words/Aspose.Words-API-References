---
title: ChartDataLabelCollection.Separator
linktitle: Separator
articleTitle: Separator
second_title: Aspose.Words per .NET
description: Scopri la proprietà Separator di ChartDataLabelCollection. Personalizza i separatori delle etichette dati per una maggiore chiarezza nei tuoi grafici, dalle virgole alle interruzioni di riga.
type: docs
weight: 90
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

Ottiene o imposta il separatore di stringa utilizzato per le etichette dati dell'intera serie. Il valore predefinito è una virgola, ad eccezione dei grafici a torta che mostrano solo il nome della categoria e la percentuale, in tal caso deve essere utilizzata un'interruzione di riga .

```csharp
public string Separator { get; set; }
```

## Osservazioni

Il valore definito per questa proprietà può essere sovrascritto per una singola etichetta dati utilizzando [`Separator`](../../chartdatalabel/separator/) proprietà.

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

Mostra come lavorare con le etichette dati di un grafico a torta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Inserire una serie di grafici personalizzati con un nome di categoria per ciascuno dei settori e la relativa tabella di frequenza.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Abilita le etichette dati che visualizzeranno sia la percentuale sia la frequenza di ciascun settore e ne modificheranno l'aspetto.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### Guarda anche

* class [ChartDataLabelCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
