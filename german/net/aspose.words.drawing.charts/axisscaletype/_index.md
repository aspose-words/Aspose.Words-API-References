---
title: Enum AxisScaleType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.AxisScaleType opsomming. Gibt die möglichen Skalentypen für eine Achse an.
type: docs
weight: 560
url: /de/net/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enumeration

Gibt die möglichen Skalentypen für eine Achse an.

```csharp
public enum AxisScaleType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Linear | `0` | Lineare Skalierung. |
| Logarithmic | `1` | Logarithmische Skalierung. |

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


