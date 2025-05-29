---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartSeries LegendEntry-Eigenschaft, um einfach auf Legendeneinträge für Ihre Diagramme zuzugreifen und diese anzupassen und so Ihre Datenvisualisierung zu verbessern.
type: docs
weight: 90
url: /de/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Ruft einen Legendeneintrag für diese Diagrammreihe ab.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Beispiele

Zeigt, wie mit einer Legendenschriftart gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Standardschriftgröße für alle Legendeneinträge festlegen.
chartLegend.Font.Size = 14;
// Schriftart für bestimmten Legendeneintrag ändern.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Legendeneintrag für Diagrammreihen abrufen.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Siehe auch

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
