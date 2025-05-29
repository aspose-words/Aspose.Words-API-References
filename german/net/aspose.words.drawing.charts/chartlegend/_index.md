---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartLegend, um Ihre Diagramme mit anpassbaren Legendeneigenschaften für eine bessere Datenvisualisierung zu verbessern.
type: docs
weight: 1010
url: /de/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Stellt die Eigenschaften der Diagrammlegende dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartLegend
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | Bietet Zugriff auf die Standardschriftformatierung von Legendeneinträgen. Um die Schriftformatierung für einen bestimmten Legendeneintrag zu überschreiben, verwenden Sie die[`Font`](../chartlegendentry/font/) Eigenschaft. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | Bietet Zugriff auf die Füll- und Linienformatierung der Legende. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Gibt eine Sammlung von Legendeneinträgen für alle Serien und Trendlinien des übergeordneten Diagramms zurück. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Legt fest, ob andere Diagrammelemente die Legende überlappen dürfen. Der Standardwert ist`FALSCH` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Gibt die Position der Legende in einem Diagramm an. |

## Beispiele

Zeigt, wie das Erscheinungsbild der Legende eines Diagramms bearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Verschieben Sie die Legende des Diagramms in die obere rechte Ecke.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Geben Sie anderen Diagrammelementen, beispielsweise dem Graphen, mehr Platz, indem Sie zulassen, dass sie die Legende überlappen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
