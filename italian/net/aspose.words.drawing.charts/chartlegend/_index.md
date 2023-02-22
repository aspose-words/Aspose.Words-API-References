---
title: Class ChartLegend
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartLegend classe. Rappresenta le proprietà della legenda del grafico.
type: docs
weight: 680
url: /it/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Rappresenta le proprietà della legenda del grafico.

```csharp
public class ChartLegend
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Restituisce una raccolta di voci di legenda per tutte le serie e le linee di tendenza del grafico principale. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Determina se altri elementi del grafico devono sovrapporsi alla legenda. Il valore predefinito è false. |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Specifica la posizione della legenda su un grafico. Il valore predefinito èRight . |

### Esempi

Mostra come modificare l'aspetto della legenda di un grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Sposta la legenda del grafico nell'angolo in alto a destra.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Concedi più spazio ad altri elementi del grafico, come il grafico, consentendo loro di sovrapporsi alla legenda.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


