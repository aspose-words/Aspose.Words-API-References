---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.ChartLegendEntry zum Erstellen dynamischer Diagrammlegenden. Verbessern Sie Ihre Datenvisualisierung durch nahtlose Integration und Anpassung.
type: docs
weight: 1020
url: /de/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Stellt einen Eintrag in der Diagrammlegende dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartLegendEntry
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Legendeneintrags. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. Der Standardwert ist**FALSCH** . |

## Bemerkungen

Ein Legendeneintrag entspricht einer bestimmten Diagrammreihe oder Trendlinie.

Der Text des Eintrags ist der Name der Serie oder Trendlinie. Der Text kann nicht geändert werden.

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
