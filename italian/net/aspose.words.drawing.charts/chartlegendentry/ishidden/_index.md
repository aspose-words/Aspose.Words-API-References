---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartLegendEntry IsHidden, controlla la visibilità della legenda del grafico senza sforzo. Migliora la presentazione dei tuoi dati con questa semplice funzione di attivazione/disattivazione!
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

Ottiene o imposta un valore che indica se questa voce è nascosta nella legenda del grafico. Il valore predefinito è**falso** .

```csharp
public bool IsHidden { get; set; }
```

## Osservazioni

Quando una voce della legenda di un grafico è nascosta, ciò non influisce sulla serie di grafici o sulla linea di tendenza corrispondente che è ancora visualizzata sul grafico.

## Esempi

Mostra come lavorare con una voce di legenda per le serie di grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### Guarda anche

* class [ChartLegendEntry](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
