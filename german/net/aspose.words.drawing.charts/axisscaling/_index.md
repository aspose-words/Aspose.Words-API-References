---
title: Class AxisScaling
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.AxisScaling klas. Stellt die Skalierungsoptionen der Achse dar.
type: docs
weight: 570
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
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | Ruft den Maximalwert der Achse ab oder setzt ihn. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | Ruft den Minimalwert der Achse ab oder legt diesen fest. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | Ruft den Skalierungstyp der Achse ab oder legt diesen fest. |

### Beispiele

Zeigt, wie eine logarithmische Skalierung auf eine Diagrammachse angewendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Eine Reihe mit X/Y-Koordinaten für fünf Punkte einfügen.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Die Skalierung der X-Achse ist standardmäßig linear,
// Anzeige gleichmäßig steigender Werte, die unseren X-Wertebereich abdecken (0, 1, 2, 3...).
// Eine lineare Achse ist für unsere Y-Werte nicht ideal
// da die Punkte mit den kleineren Y-Werten schwerer zu lesen sind.
// Eine logarithmische Skalierung mit einer Basis von 20 (1, 20, 400, 8000...)
// verteilt die gezeichneten Punkte, sodass wir ihre Werte im Diagramm leichter ablesen können.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


