---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.ChartAxisCollection, Ihre Lösung für die effiziente Verwaltung von Diagrammachsen und die Verbesserung der Datenvisualisierung Ihres Dokuments.
type: docs
weight: 900
url: /de/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Stellt eine Sammlung von Diagrammachsen dar.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Ruft die Anzahl der Achsen in dieser Sammlung ab. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Ruft die Achse am angegebenen Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

## Beispiele

Zeigt, wie mit der Achsensammlung gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Blenden Sie die Hauptgitterlinien auf der primären und sekundären Y-Achse aus.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Siehe auch

* class [ChartAxis](../chartaxis/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
