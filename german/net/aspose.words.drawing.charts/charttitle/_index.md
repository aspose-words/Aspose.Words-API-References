---
title: Class ChartTitle
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartTitle klas. Bietet Zugriff auf die Eigenschaften des Diagrammtitels.
type: docs
weight: 820
url: /de/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Bietet Zugriff auf die Eigenschaften des Diagrammtitels.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartTitle
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } |  |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Legt fest, ob andere Diagrammelemente den Titel überlappen dürfen. Standardmäßig ist Overlay`FALSCH` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Legt fest, ob der Titel für dieses Diagramm angezeigt werden soll. Der Standardwert ist`WAHR` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Ruft den Text des Diagrammtitels ab oder legt ihn fest. Wenn`Null` oder ein leerer Wert angegeben wird, wird der automatisch generierte Titel angezeigt. |

### Beispiele

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


