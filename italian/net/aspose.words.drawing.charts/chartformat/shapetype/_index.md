---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà ShapeType di ChartFormat per personalizzare efficacemente gli elementi del tuo grafico. Migliora la tua visualizzazione dei dati oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

Ottiene o imposta il tipo di forma dell'elemento del grafico padre.

```csharp
public ChartShapeType ShapeType { get; set; }
```

## Osservazioni

Attualmente, la proprietà può essere utilizzata solo per le etichette dati.

## Esempi

Mostra come impostare la formattazione di riempimento, tratto e callout per le etichette dei dati del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Elimina la serie generata di default.
chart.Series.Clear();

// Aggiungi nuova serie.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Mostra le etichette dei dati.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Formatta le etichette dati come callout.
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

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
