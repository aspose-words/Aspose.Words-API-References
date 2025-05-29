---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words per .NET
description: Personalizza l'orientamento delle tue etichette AxisTickLabels per una leggibilità ottimale. Regola facilmente la direzione del testo delle etichette di spunta per migliorare la visualizzazione dei tuoi dati!
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

Ottiene o imposta l'orientamento del testo dell'etichetta di spunta.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Osservazioni

Il valore predefinito èHorizontal.

Nota che alcuni[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) i valori non influenzano l'orientamento dell'etichetta di spunta text negli assi dei valori.

## Esempi

Mostra come modificare l'orientamento e la rotazione delle etichette delle tacche degli assi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a colonne.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Imposta l'orientamento e la rotazione dell'etichetta di spunta dell'asse.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### Guarda anche

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
