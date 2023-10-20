---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.Charts.ChartAxisCollection classe. Rappresenta una raccolta di assi del grafico in C#.
type: docs
weight: 640
url: /it/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Rappresenta una raccolta di assi del grafico.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Ottiene il numero di assi in questa raccolta. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Ottiene l'asse all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Restituisce un oggetto enumeratore. |

## Esempi

Mostra come lavorare con la raccolta degli assi.

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

* class [ChartAxis](../chartaxis/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
