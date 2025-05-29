---
title: AxisScaling Class
linktitle: AxisScaling
articleTitle: AxisScaling
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.AxisScaling für anpassbare Achsenskalierungsoptionen, mit denen Sie Ihre Diagrammpräsentationen mühelos verbessern können.
type: docs
weight: 820
url: /de/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

Stellt die Skalierungsoptionen der Achse dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class AxisScaling
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [AxisScaling](axisscaling/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | Ruft die logarithmische Basis für eine logarithmische Achse ab oder legt sie fest. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | Ruft den Maximalwert der Achse ab oder legt ihn fest. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | Ruft den Mindestwert der Achse ab oder legt ihn fest. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | Ruft den Skalierungstyp der Achse ab oder legt ihn fest. |

## Beispiele

Zeigt, wie man eine logarithmische Skalierung auf eine Diagrammachse anwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügt eine Reihe mit X/Y-Koordinaten für fünf Punkte ein.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Die Skalierung der X-Achse ist standardmäßig linear,
// Anzeige gleichmäßig steigender Werte, die unseren X-Wertebereich (0, 1, 2, 3 ...) abdecken.
// Eine lineare Achse ist für unsere Y-Werte nicht ideal
// da die Punkte mit den kleineren Y-Werten schwerer zu lesen sind.
// Eine logarithmische Skalierung mit einer Basis von 20 (1, 20, 400, 8000...)
// verteilt die dargestellten Punkte, sodass wir ihre Werte im Diagramm leichter ablesen können.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
