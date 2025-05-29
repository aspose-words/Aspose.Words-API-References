---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words per .NET
description: Applica stili di grafico predefiniti in Aspose.Words. Migliora gli elementi visivi con l'enumerazione ChartStyle per una formattazione professionale dei documenti.
type: docs
weight: 1130
url: /it/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Specifica gli stili predefiniti di un grafico.

```csharp
public enum ChartStyle
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normal | `0` | Rappresenta lo stile grafico predefinito. |
| Muted | `1` | Uno stile con colori tenui. |
| Saturated | `2` | Uno stile con colori più saturi. |
| Shaded | `3` | Uno stile con punti dati ombreggiati. |
| Flat | `4` | Uno stile con punti dati piatti senza sfumatura. |
| Shadowed | `5` | Uno stile con punti dati con un'ombra. |
| Gradient | `6` | Uno stile con riempimento sfumato dei punti dati. |
| Original | `7` | Uno stile con l'aspetto originale di un grafico. |
| Transparent1 | `8` | Uno stile con punti dati trasparenti. |
| Transparent2 | `9` | Uno stile con punti dati trasparenti. |
| Outline | `10` | Uno stile con punti dati senza riempimento, ma solo con contorno. |
| OutlineBlack | `11` | Uno stile con sfondo grafico nero, in cui i punti dati non hanno riempimento, ma solo un contorno. |
| Black | `12` | Uno stile con sfondo grafico nero. |
| Grey | `13` | Uno stile con sfondo grafico sfumato grigio. |
| Blue | `14` | Uno stile con sfondo grafico blu. |
| ShadedPlot | `15` | Uno stile in cui l'area del grafico è ombreggiata. |

## Esempi

Mostra come impostare e ottenere lo stile del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico in stile Nero.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Ottieni un grafico da aggiornare.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Ottieni lo stile del grafico.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
