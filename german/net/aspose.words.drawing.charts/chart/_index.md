---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words für .NET
description: Schalten Sie leistungsstarke Diagrammformeigenschaften mit der Klasse Aspose.Words.Drawing.Charts.Chart frei. Optimieren Sie Ihre Dokumente mit dynamischer visueller Datendarstellung.
type: docs
weight: 880
url: /de/net/aspose.words.drawing.charts/chart/
---
## Chart class

Bietet Zugriff auf die Eigenschaften der Diagrammform.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class Chart
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | Ruft eine Sammlung aller Achsen dieses Diagramms ab. |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Bietet Zugriff auf die Eigenschaften der primären X-Achse des Diagramms. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Bietet Zugriff auf die Eigenschaften der primären Y-Achse des Diagramms. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Bietet Zugriff auf die Eigenschaften der Z-Achse des Diagramms. |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | Bietet Zugriff auf die Eigenschaften einer Datentabelle dieses Diagramms. Die Datentabelle kann angezeigt werden mit dem[`Show`](../chartdatatable/show/) Eigenschaft. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | Bietet Zugriff auf die Füll- und Linienformatierung des Diagramms. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Bietet Zugriff auf die Eigenschaften der Diagrammlegende. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Bietet Zugriff auf die Seriensammlung. |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | Bietet Zugriff auf eine Seriengruppensammlung dieses Diagramms. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Ruft den Pfad und Namen einer XLS-/XLSX-Datei ab, mit der dieses Diagramm verknüpft ist. |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | Ruft den Stil des Diagramms ab oder legt ihn fest. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Bietet Zugriff auf die Eigenschaften des Diagrammtitels. |

## Beispiele

Zeigt, wie Sie ein Diagramm einfügen und einen Titel festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie mit einem Dokumentgenerator eine Diagrammform ein und rufen Sie das Diagramm ab.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Verwenden Sie die Eigenschaft „Titel“, um unserem Diagramm einen Titel zu geben, der oben in der Mitte des Diagrammbereichs angezeigt wird.
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

    // Setzen Sie die Eigenschaft „Anzeigen“ auf „true“, um den Titel sichtbar zu machen.
title.Show = true;

// Setzen Sie die Eigenschaft „Overlay“ auf „true“. Geben Sie anderen Diagrammelementen mehr Platz, indem Sie ihnen erlauben, den Titel zu überlappen
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
