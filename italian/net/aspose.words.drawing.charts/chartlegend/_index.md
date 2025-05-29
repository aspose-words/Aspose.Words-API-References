---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartLegend per migliorare i tuoi grafici con proprietà di legenda personalizzabili per una migliore visualizzazione dei dati.
type: docs
weight: 1010
url: /it/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Rappresenta le proprietà della legenda del grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartLegend
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | Fornisce l'accesso alla formattazione predefinita del carattere per le voci della legenda. Per sovrascrivere la formattazione del carattere per una specifica voce della legenda, utilizzare[`Font`](../chartlegendentry/font/) proprietà. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | Fornisce accesso al riempimento e alla formattazione delle linee della legenda. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Restituisce una raccolta di voci della legenda per tutte le serie e le linee di tendenza del grafico padre. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Determina se altri elementi del grafico possono sovrapporsi alla legenda. Il valore predefinito è`falso` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Specifica la posizione della legenda su un grafico. |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
