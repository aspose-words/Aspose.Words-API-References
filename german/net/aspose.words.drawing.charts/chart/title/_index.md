---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words für .NET
description: Chart Title eigendom. Bietet Zugriff auf die Eigenschaften des Diagrammtitels in C#.
type: docs
weight: 80
url: /de/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

Bietet Zugriff auf die Eigenschaften des Diagrammtitels.

```csharp
public ChartTitle Title { get; }
```

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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
