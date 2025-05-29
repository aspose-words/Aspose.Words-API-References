---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words per .NET
description: Scopri la proprietà Sovrapposizione di ChartSeriesGroup per regolare facilmente la percentuale di sovrapposizione delle barre o delle colonne della serie per una migliore visualizzazione dei dati.
type: docs
weight: 80
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Ottiene o imposta la percentuale di sovrapposizione delle barre o delle colonne della serie.

```csharp
public int Overlap { get; set; }
```

## Osservazioni

Si applica ai gruppi di serie di tutti i tipi di barre e colonne.

L'intervallo di valori accettabili è compreso tra -100 e 100 (inclusi). Un valore pari a 0 indica che non c'è spazio tra barre/colonne. Se il valore è -100, la distanza tra barre/colonne è pari alla loro larghezza. Un valore pari a 100 indica che le barre/colonne si sovrappongono completamente.

## Esempi

Mostra come configurare la larghezza e la sovrapposizione degli spazi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Imposta la larghezza dello spazio tra le colonne e la sovrapposizione.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Guarda anche

* class [ChartSeriesGroup](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
