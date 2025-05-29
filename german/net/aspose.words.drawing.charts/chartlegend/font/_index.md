---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Passen Sie die Schrifteinstellungen Ihrer ChartLegend mühelos an! Greifen Sie auf die Standardformatierung zu und überschreiben Sie bestimmte Legendeneinträge ganz einfach für ein ansprechendes Erscheinungsbild.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

Bietet Zugriff auf die Standardschriftformatierung von Legendeneinträgen. Um die Schriftformatierung für einen bestimmten Legendeneintrag zu überschreiben, verwenden Sie die[`Font`](../../chartlegendentry/font/) Eigenschaft.

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
* class [ChartLegend](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
