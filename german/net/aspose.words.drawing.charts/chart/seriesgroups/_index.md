---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words für .NET
description: Erkunden Sie die Eigenschaft „Chart SeriesGroups“, um einfach auf eine umfangreiche Sammlung von Seriengruppen zuzugreifen und so Ihr Erlebnis der Datenvisualisierung zu verbessern.
type: docs
weight: 90
url: /de/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Bietet Zugriff auf eine Seriengruppensammlung dieses Diagramms.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
