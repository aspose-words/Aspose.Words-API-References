---
title: ChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartDataPoint-Explosion-Eigenschaft, um Kreisdiagramm-Datenpunkte anzupassen. Steuern Sie die Bewegung vom Zentrum aus für wirkungsvolle Visualisierungen. Optimieren Sie Ihre Diagramme noch heute!
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartdatapoint/explosion/
---
## ChartDataPoint.Explosion property

Gibt den Betrag an, um den der Datenpunkt von der Mitte des Kreisdiagramms verschoben werden soll. Kann negativ sein. Negativ bedeutet, dass die Eigenschaft nicht festgelegt ist und keine Explosion angewendet werden soll. Gilt nur für Kreisdiagramme.

```csharp
public int Explosion { get; set; }
```

## Beispiele

Zeigt, wie die Segmente eines Kreisdiagramms von der Mitte weg verschoben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// „Stücke“ eines Kreisdiagramms können über das Explosionsattribut des jeweiligen Datenpunkts um eine gewisse Distanz vom Mittelpunkt weg verschoben werden.
// Fügen Sie dem ersten Teil des Kreisdiagramms einen Datenpunkt hinzu und verschieben Sie ihn um 10 Punkte von der Mitte weg.
// Aspose.Words erstellt automatisch Datenpunkte, wenn diese nicht vorhanden sind.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Verschiebe den zweiten Teil um eine größere Distanz.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Siehe auch

* class [ChartDataPoint](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
