---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words per .NET
description: Regola la rotazione di AxisTickLabels per una leggibilità ottimale. Personalizza l'angolazione delle etichette di graduazione in gradi per migliorare la chiarezza e l'aspetto visivo del tuo grafico.
type: docs
weight: 70
url: /it/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

Ottiene o imposta la rotazione delle etichette delle tacche in gradi.

```csharp
public int Rotation { get; set; }
```

## Osservazioni

L'intervallo di valori accettabili è compreso tra -180 e 180 (inclusi). Il valore predefinito è 0.

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

* class [AxisTickLabels](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
