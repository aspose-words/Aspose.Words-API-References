---
title: AxisScaling.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Achsenskalierungstyp“, um Ihre Achsenskalierung einfach anzupassen. Verbessern Sie Ihre Datenvisualisierung mit flexiblen Einstellungen für optimale Übersichtlichkeit.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/axisscaling/type/
---
## AxisScaling.Type property

Ruft den Skalierungstyp der Achse ab oder legt ihn fest.

```csharp
public AxisScaleType Type { get; set; }
```

## Bemerkungen

DieLinearWert ist der einzige, der in den neuen Diagrammen von MS Office 2016 zulässig ist.

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

* enum [AxisScaleType](../../axisscaletype/)
* class [AxisScaling](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
