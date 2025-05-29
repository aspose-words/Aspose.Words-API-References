---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words für .NET
description: Entdecken Sie die Überlappungseigenschaft von ChartSeriesGroup, um den Überlappungsprozentsatz Ihrer Serienbalken oder -spalten einfach anzupassen und so die Datenvisualisierung zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Ruft den Prozentsatz ab, um den sich die Balken oder Spalten der Serie überlappen, oder legt diesen fest.

```csharp
public int Overlap { get; set; }
```

## Bemerkungen

Gilt für Seriengruppen aller Balken- und Säulentypen.

Der zulässige Wertebereich liegt zwischen -100 und 100 (einschließlich). Ein Wert von 0 bedeutet, dass zwischen den Balken/Spalten kein Abstand besteht. Bei einem Wert von -100 entspricht der Abstand zwischen den Balken/Spalten ihrer Breite. Ein Wert von 100 bedeutet, dass sich die Balken/Spalten vollständig überlappen.

## Beispiele

Zeigen Sie, wie Sie Spaltbreite und Überlappung konfigurieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Spaltenabstandsbreite und Überlappung festlegen.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Siehe auch

* class [ChartSeriesGroup](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
