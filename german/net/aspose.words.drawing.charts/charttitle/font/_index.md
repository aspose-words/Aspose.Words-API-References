---
title: ChartTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words für .NET
description: Passen Sie Ihren Diagrammtitel mit der ChartTitle-Schriftarteigenschaft für eine verbesserte Schriftformatierung an. Verbessern Sie Ihre Datenpräsentation mühelos!
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/charttitle/font/
---
## ChartTitle.Font property

Bietet Zugriff auf die Schriftformatierung des Diagrammtitels.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ChartTitle](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
