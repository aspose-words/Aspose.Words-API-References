---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words per .NET
description: Esplora la proprietà Chart SeriesGroups per accedere facilmente a una vasta raccolta di gruppi di serie, migliorando la tua esperienza di visualizzazione dei dati.
type: docs
weight: 90
url: /it/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Fornisce l'accesso a una raccolta di gruppi di serie di questo grafico.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
