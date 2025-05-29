---
title: ChartDataLabelCollection.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words per .NET
description: Scopri la proprietà Orientamento di ChartDataLabelCollection per personalizzare facilmente l'orientamento del testo per le etichette dati, migliorando la chiarezza e l'impatto del grafico.
type: docs
weight: 60
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---
## ChartDataLabelCollection.Orientation property

Ottiene o imposta l'orientamento del testo delle etichette dati dell'intera serie.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Osservazioni

Il valore predefinito èHorizontal .

## Esempi

Mostra come modificare l'orientamento e la rotazione delle etichette dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Mostra le etichette dei dati.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Definisce la forma dell'etichetta dati.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Imposta l'orientamento e la rotazione dell'etichetta dati per l'intera serie.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// Modifica l'orientamento e la rotazione della prima etichetta dati.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### Guarda anche

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabelCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
