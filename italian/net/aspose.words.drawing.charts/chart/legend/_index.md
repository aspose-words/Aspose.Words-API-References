---
title: Chart.Legend
second_title: Aspose.Words per .NET API Reference
description: Chart proprietà. Fornisce laccesso alle proprietà della legenda del grafico.
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Fornisce l'accesso alle proprietà della legenda del grafico.

```csharp
public ChartLegend Legend { get; }
```

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chart/)
* assemblea [Aspose.Words](../../../)


