---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartSeriesGroup GapWidth-Eigenschaft, um den Abstand zwischen Diagrammelementen in Prozent einfach anzupassen und so die Datenvisualisierung zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Ruft den Prozentsatz der Lückenbreite zwischen Diagrammelementen ab oder legt ihn fest.

```csharp
public int GapWidth { get; set; }
```

## Bemerkungen

Gilt nur für Reihengruppen der Typen Balken, Säulen, Kreisdiagramme, Kreisdiagramme, Histogramme, Box&amp;Whisker, Wasserfall und Trichter.

Der zulässige Wertebereich reicht von 0 bis einschließlich 500. Bei balken-/spaltenbasierten Reihengruppen stellt die Eigenschaft den Abstand zwischen Balkenclustern als Prozentsatz ihrer Breite dar. Bei Kreis-aus-Kreis- und Balken-aus-Kreis-Diagrammen ist dies der Abstand zwischen dem primären und sekundären Abschnitt des Diagramms.

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
