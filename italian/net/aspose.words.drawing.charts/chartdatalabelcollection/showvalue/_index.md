---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ShowValue in ChartDataLabelCollection migliora la visualizzazione dei dati mostrando i valori delle serie. Ottimizza i tuoi grafici oggi stesso!
type: docs
weight: 170
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Consente di specificare se i valori devono essere visualizzati nelle etichette dati dell'intera serie. Il valore predefinito è`falso` .

```csharp
public bool ShowValue { get; set; }
```

## Osservazioni

Il valore definito per questa proprietà può essere sovrascritto per una singola etichetta dati utilizzando [`ShowValue`](../../chartdatalabel/showvalue/) proprietà.

## Esempi

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
