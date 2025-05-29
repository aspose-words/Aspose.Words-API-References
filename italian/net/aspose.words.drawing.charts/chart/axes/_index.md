---
title: Chart.Axes
linktitle: Axes
articleTitle: Axes
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Assi grafico" per accedere facilmente a tutti gli assi del grafico. Migliora la visualizzazione dei dati con una gestione completa degli assi.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Ottiene una raccolta di tutti gli assi di questo grafico.

```csharp
public ChartAxisCollection Axes { get; }
```

## Esempi

Mostra come lavorare con la raccolta di assi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Nasconde le linee principali della griglia sugli assi Y primario e secondario.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Guarda anche

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
