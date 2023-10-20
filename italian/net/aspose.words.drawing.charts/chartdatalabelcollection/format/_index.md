---
title: ChartDataLabelCollection.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words per .NET
description: ChartDataLabelCollection Format proprietà. Fornisce laccesso al riempimento e alla formattazione della riga delle etichette dati in C#.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

Fornisce l'accesso al riempimento e alla formattazione della riga delle etichette dati.

```csharp
public ChartFormat Format { get; }
```

## Esempi

Mostra come impostare la formattazione di riempimento, tratto e didascalia per le etichette dei dati del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Elimina le serie generate predefinite.
chart.Series.Clear();

// Aggiunge una nuova serie.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Mostra le etichette dei dati.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Formatta le etichette dei dati come callout.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Modifica il riempimento e il tratto di una singola etichetta dati.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Guarda anche

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
