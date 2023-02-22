---
title: ChartDataLabelCollection.ShowPercentage
second_title: Aspose.Words per .NET API Reference
description: ChartDataLabelCollection proprietà. Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dati dellintera serie. Il valore di default è falso . Si applica solo ai grafici a torta.
type: docs
weight: 100
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/
---
## ChartDataLabelCollection.ShowPercentage property

Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dati dell'intera serie. Il valore di default è **falso** . Si applica solo ai grafici a torta.

```csharp
public bool ShowPercentage { get; set; }
```

### Osservazioni

Il valore definito per questa proprietà può essere sovrascritto per una singola etichetta dati utilizzando [`ShowPercentage`](../../chartdatalabel/showpercentage/) proprietà.

### Esempi

Mostra come lavorare con le etichette dati di un grafico a torta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Inserisce una serie di grafici personalizzata con un nome di categoria per ciascuno dei settori e la relativa tabella di frequenza.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Abilita le etichette dei dati che visualizzeranno sia la percentuale che la frequenza di ciascun settore e ne modificheranno l'aspetto.
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
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* assemblea [Aspose.Words](../../../)


