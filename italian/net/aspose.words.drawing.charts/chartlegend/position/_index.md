---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words per .NET
description: Scopri la proprietà Posizione ChartLegend per personalizzare facilmente il posizionamento della legenda del tuo grafico, per una maggiore chiarezza e un impatto visivo più gradevole.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Specifica la posizione della legenda su un grafico.

```csharp
public LegendPosition Position { get; set; }
```

## Osservazioni

Il valore predefinito èRight per grafici pre-Word 2016 e Top per grafici di Word 2016.

## Esempi

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

// Lascia più spazio agli altri elementi del grafico, come il grafico stesso, sovrapponendoli alla legenda.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Guarda anche

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
