---
title: IChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words für .NET
description: IChartDataPoint Explosion eigendom. Gibt den Betrag an um den der Datenpunkt von der Mitte des Kreises verschoben werden soll. Kann negativ sein. Negativ bedeutet dass die Eigenschaft nicht festgelegt ist und keine Explosion angewendet werden soll. Gilt nur für Kreisdiagramme in C#.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Gibt den Betrag an, um den der Datenpunkt von der Mitte des Kreises verschoben werden soll. Kann negativ sein. Negativ bedeutet, dass die Eigenschaft nicht festgelegt ist und keine Explosion angewendet werden soll. Gilt nur für Kreisdiagramme.

```csharp
public int Explosion { get; set; }
```

## Beispiele

Zeigt, wie die Abschnitte eines Kreisdiagramms von der Mitte weg verschoben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// „Slices“ eines Kreisdiagramms können über das Explosionsattribut des jeweiligen Datenpunkts um eine Distanz von der Mitte entfernt werden.
// Fügen Sie einen Datenpunkt zum ersten Teil des Kreisdiagramms hinzu und verschieben Sie ihn um 10 Punkte von der Mitte weg.
// Aspose.Words erstellt automatisch Datenpunkte, wenn diese nicht vorhanden sind.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Den zweiten Teil um eine größere Distanz verschieben.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Siehe auch

* interface [IChartDataPoint](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
