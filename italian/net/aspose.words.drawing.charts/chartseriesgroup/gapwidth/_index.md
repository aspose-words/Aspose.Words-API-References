---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words per .NET
description: Scopri la proprietà GapWidth di ChartSeriesGroup per regolare facilmente la percentuale di spazio tra gli elementi del grafico e ottenere una migliore visualizzazione dei dati.
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Ottiene o imposta la percentuale di larghezza dello spazio tra gli elementi del grafico.

```csharp
public int GapWidth { get; set; }
```

## Osservazioni

Si applica solo ai gruppi di serie di tipo a barre, a colonne, a torta di barre, a torta di torta, a istogramma, a scatola e baffi, a cascata e a imbuto.

L'intervallo di valori accettabili è compreso tra 0 e 500 (inclusi). Per i gruppi di serie basati su barre/colonne, la proprietà rappresenta lo spazio tra i cluster di barre come percentuale della loro larghezza. Per i grafici a torta e a barre , questo è lo spazio tra la sezione primaria e quella secondaria del grafico.

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
