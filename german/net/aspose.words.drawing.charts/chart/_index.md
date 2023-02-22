---
title: Class Chart
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.Chart klas. Bietet Zugriff auf die Eigenschaften der Diagrammform.
type: docs
weight: 600
url: /de/net/aspose.words.drawing.charts/chart/
---
## Chart class

Bietet Zugriff auf die Eigenschaften der Diagrammform.

```csharp
public class Chart
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | Bietet Zugriff auf Eigenschaften der X-Achse des Diagramms. |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | Bietet Zugriff auf Eigenschaften der Y-Achse des Diagramms. |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | Bietet Zugriff auf Eigenschaften der Z-Achse des Diagramms. |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | Bietet Zugriff auf die Eigenschaften der Diagrammlegende. |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | Bietet Zugriff auf die Seriensammlung. |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | Ruft den Pfad und Namen einer xls/xlsx-Datei ab, mit der dieses Diagramm verknüpft ist. |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | Bietet Zugriff auf die Eigenschaften des Diagrammtitels. |

### Beispiele

Zeigt, wie Sie ein Diagramm einfügen und einen Titel festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Diagrammform mit einem Dokumentenersteller ein und erhalten Sie ihr Diagramm.
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// Verwenden Sie die Eigenschaft "Titel", um unserem Diagramm einen Titel zu geben, der oben in der Mitte des Diagrammbereichs angezeigt wird.
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // Setzen Sie die Eigenschaft "Show" auf "true", um den Titel sichtbar zu machen.
title.Show = true;

// Setzen Sie die Eigenschaft "Overlay" auf "true". Geben Sie anderen Diagrammelementen mehr Platz, indem Sie ihnen erlauben, den Titel zu überlappen
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


