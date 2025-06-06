---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words per .NET
description: Sovrapposizione degli elementi del grafico di controllo con la proprietà ChartLegend Overlay. Migliora la visualizzazione dei dati con impostazioni di legenda personalizzabili per informazioni più chiare.
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

Determina se altri elementi del grafico possono sovrapporsi alla legenda. Il valore predefinito è`falso` .

```csharp
public bool Overlay { get; set; }
```

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

* class [ChartLegend](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
