---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartTitle, um Ihre Diagrammtitel für eine verbesserte Datenvisualisierung einfach zu verwalten und anzupassen.
type: docs
weight: 1140
url: /de/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

Bietet Zugriff auf die Eigenschaften des Diagrammtitels.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit -Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartTitle
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | Bietet Zugriff auf die Schriftformatierung des Diagrammtitels. |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | Bietet Zugriff auf die Füll- und Linienformatierung des Diagrammtitels. |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | Legt fest, ob andere Diagrammelemente den Titel überlappen dürfen. Standardmäßig ist die Überlagerung`FALSCH` . |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | Legt fest, ob der Titel für dieses Diagramm angezeigt werden soll. Der Standardwert ist`WAHR` . |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | Ruft den Text des Diagrammtitels ab oder legt ihn fest. Wenn`null` oder ein leerer Wert angegeben wird, wird ein automatisch generierter Titel angezeigt. |

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
