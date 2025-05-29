---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.ShapeTextOrientation per controllare facilmente l'orientamento del testo nelle forme, migliorando la progettazione e la leggibilità dei tuoi documenti.
type: docs
weight: 1680
url: /it/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Specifica l'orientamento del testo nelle forme.

```csharp
public enum ShapeTextOrientation
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Horizontal | `0` | Il testo è disposto orizzontalmente (lr-tb). |
| Downward | `1` | Il testo viene ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl). |
| Upward | `2` | Il testo viene ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr). |
| VerticalFarEast | `3` | I caratteri dell'Estremo Oriente appaiono in verticale, il resto del testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v). |
| VerticalRotatedFarEast | `4` | I caratteri dell'Estremo Oriente appaiono in verticale, il resto del testo viene ruotato di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, quindi da sinistra a destra orizzontalmente (tb-lr-v). |
| WordArtVertical | `5` | Il testo è verticale, con una lettera sopra l'altra. |
| WordArtVerticalRightToLeft | `6` | Il testo è verticale, con una lettera sopra l'altra, poi da destra a sinistra orizzontalmente. |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
