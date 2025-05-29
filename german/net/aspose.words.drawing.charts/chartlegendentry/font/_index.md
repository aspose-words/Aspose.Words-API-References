---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Entdecken Sie die Schriftarteigenschaft „ChartLegendEntry“ für einfachen Zugriff auf anpassbare Schriftformatierungen und verbessern Sie so die visuelle Attraktivität Ihrer Legendeneinträge.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Bietet Zugriff auf die Schriftformatierung dieses Legendeneintrags.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
