---
title: AxisScaling.LogBase
linktitle: LogBase
articleTitle: LogBase
second_title: Aspose.Words für .NET
description: Passen Sie die logarithmische Basis der AxisScaling LogBase-Eigenschaft für eine präzise Datenvisualisierung und verbesserte Diagrammgenauigkeit an. Optimieren Sie Ihre Diagramme noch heute!
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

Ruft die logarithmische Basis für eine logarithmische Achse ab oder legt sie fest.

```csharp
public double LogBase { get; set; }
```

## Bemerkungen

Die Eigenschaft wird von den neuen Diagrammen von MS Office 2016 nicht unterstützt.

Der gültige Bereich eines Gleitkommawerts ist größer oder gleich 2 und kleiner oder gleich 1000. Die Eigenschaft ist nur wirksam, wenn[`Type`](../type/) ist auf eingestelltLogarithmic.

Durch das Setzen dieser Eigenschaft wird die[`Type`](../type/) Eigentum zuLogarithmic .

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

* class [AxisScaling](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
