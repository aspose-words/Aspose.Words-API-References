---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words per .NET
description: Scopri la proprietà BubbleScale di ChartSeriesGroup per personalizzare le dimensioni delle bolle nei tuoi grafici, migliorando la visualizzazione dei dati e il coinvolgimento degli utenti.
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Ottiene o imposta la dimensione delle bolle come percentuale della loro dimensione predefinita.

```csharp
public int BubbleScale { get; set; }
```

## Osservazioni

Si applica solo ai gruppi di serie diBubble e Bubble3D tipi.

L'intervallo di valori accettabili è compreso tra 0 e 300 (inclusi). Il valore predefinito è 100.

## Esempi

Mostra come impostare la dimensione delle bolle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a bolle 3D.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Imposta la scala della bolla al 200%.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### Guarda anche

* class [ChartSeriesGroup](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
