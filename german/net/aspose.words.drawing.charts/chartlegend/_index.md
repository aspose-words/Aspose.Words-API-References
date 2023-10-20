---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.Charts.ChartLegend klas. Stellt die Eigenschaften der Diagrammlegende dar in C#.
type: docs
weight: 720
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
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Gibt eine Sammlung von Legendeneinträgen für alle Serien und Trendlinien des übergeordneten Diagramms zurück. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Legt fest, ob andere Diagrammelemente die Legende überlappen dürfen. Der Standardwert ist`FALSCH` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Gibt die Position der Legende in einem Diagramm an. Der Standardwert istRight . |

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

// Die Legende des Diagramms in die obere rechte Ecke verschieben.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Geben Sie anderen Diagrammelementen, z. B. dem Diagramm, mehr Platz, indem Sie ihnen erlauben, die Legende zu überlappen.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
