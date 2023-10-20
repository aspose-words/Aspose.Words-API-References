---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.Charts.Chart klas. Bietet Zugriff auf die Diagrammformeigenschaften in C#.
type: docs
weight: 620
url: /de/net/aspose.words.drawing.charts/chart/
---
## Chart class

Bietet Zugriff auf die Diagrammformeigenschaften.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class Chart
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Ruft eine Sammlung aller Achsen dieses Diagramms ab. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Bietet Zugriff auf Eigenschaften der X-Achse des Diagramms. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Bietet Zugriff auf Eigenschaften der Y-Achse des Diagramms. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Bietet Zugriff auf Eigenschaften der Z-Achse des Diagramms. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Bietet Zugriff auf die Eigenschaften der Diagrammlegende. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Bietet Zugriff auf die Seriensammlung. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Ruft den Pfad und Namen einer XLS/XLSX-Datei ab, mit der dieses Diagramm verknüpft ist. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Bietet Zugriff auf die Eigenschaften des Diagrammtitels. |

## Beispiele

Zeigt, wie man ein Diagramm einfügt und einen Titel festlegt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Mit einem Document Builder eine Diagrammform einfügen und das zugehörige Diagramm abrufen.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Verwenden Sie die Eigenschaft „Title“, um unserem Diagramm einen Titel zu geben, der oben in der Mitte des Diagrammbereichs angezeigt wird.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Setzen Sie die Eigenschaft „Show“ auf „true“, um den Titel sichtbar zu machen.
title.Show = true;

// Setzen Sie die Eigenschaft „Overlay“ auf „true“. Geben Sie anderen Diagrammelementen mehr Platz, indem Sie ihnen erlauben, den Titel zu überlappen
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
