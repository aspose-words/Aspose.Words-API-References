---
title: Class ChartTitle
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartTitle klas. Bietet Zugriff auf die Eigenschaften des Diagrammtitels.
type: docs
weight: 750
url: /de/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Bietet Zugriff auf die Eigenschaften des Diagrammtitels.

```csharp
public class ChartTitle
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Legt fest, ob andere Diagrammelemente den Titel überlappen dürfen. Standardmäßig ist Überlagerung falsch. |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Legt fest, ob der Titel für dieses Diagramm angezeigt werden soll. Standardwert ist wahr. |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Ruft den Text des Diagrammtitels ab oder legt ihn fest. Wenn ein Null- oder leerer Wert angegeben wird, wird der automatisch generierte Titel angezeigt. |

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


