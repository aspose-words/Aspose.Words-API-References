---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartSeries LegendEntry per accedere e personalizzare facilmente le voci della legenda per i tuoi grafici, migliorando la visualizzazione dei dati.
type: docs
weight: 90
url: /it/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Ottiene una voce di legenda per questa serie di grafici.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Esempi

Mostra come lavorare con un font di legenda.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Imposta la dimensione predefinita del carattere per tutte le voci della legenda.
chartLegend.Font.Size = 14;
// Cambia il font per una voce specifica della legenda.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Ottieni la voce della legenda per la serie di grafici.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Guarda anche

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
