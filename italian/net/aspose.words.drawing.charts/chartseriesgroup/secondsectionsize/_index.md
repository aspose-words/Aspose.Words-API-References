---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words per .NET
description: Scopri come modificare la proprietà SecondSectionSize in ChartSeriesGroup per personalizzare in modo efficace le dimensioni della sezione secondaria del tuo grafico a torta.
type: docs
weight: 90
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Ottiene o imposta la dimensione della sezione secondaria del grafico a torta in percentuale.

```csharp
public int SecondSectionSize { get; set; }
```

## Osservazioni

Si applica ai gruppi di serie diPieOfPie e PieOfBar tipi.

L'intervallo di valori accettabili è compreso tra 5 e 200 (inclusi). Il valore predefinito è 75.

## Esempi

Mostra come creare e formattare un grafico a torta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// Elimina la serie generata di default.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Formatta il grafico a torta.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### Guarda anche

* class [ChartSeriesGroup](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
