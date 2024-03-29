---
title: ChartDataPoint.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words per .NET
description: ChartDataPoint Format proprietà. Fornisce laccesso al riempimento e alla formattazione della linea di questo punto dati in C#.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Fornisce l'accesso al riempimento e alla formattazione della linea di questo punto dati.

```csharp
public ChartFormat Format { get; }
```

## Esempi

Mostra come impostare la formattazione individuale per le categorie di un grafico a colonne.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Elimina le serie generate predefinite.
chart.Series.Clear();

// Aggiunta di nuove serie.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Imposta la formattazione della colonna.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

### Guarda anche

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
