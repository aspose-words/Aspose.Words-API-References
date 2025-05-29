---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartDataLabel Rotation per personalizzare facilmente l'angolazione delle etichette nei tuoi grafici. Migliora la visualizzazione dei dati con un controllo preciso!
type: docs
weight: 110
url: /it/net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

Ottiene o imposta la rotazione dell'etichetta in gradi.

```csharp
public int Rotation { get; set; }
```

## Osservazioni

L'intervallo di valori accettabili è compreso tra -180 e 180 (inclusi). Il valore predefinito è 0.

Se il[`Orientation`](../orientation/) il valore èHorizontal la forma dell'etichetta , se esiste, viene ruotata insieme al testo dell'etichetta. In caso contrario, viene ruotato solo il testo dell'etichetta.

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

* class [ChartDataLabel](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
