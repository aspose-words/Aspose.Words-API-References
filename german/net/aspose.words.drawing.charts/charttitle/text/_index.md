---
title: ChartTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Passen Sie Ihren Diagrammtitel mühelos an! Legen Sie die Texteigenschaft „ChartTitle“ fest oder rufen Sie sie ab, um eine persönliche Note zu erhalten. Titel werden bei Bedarf automatisch generiert.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Ruft den Text des Diagrammtitels ab oder legt ihn fest. Wenn`null` oder ein leerer Wert angegeben wird, wird ein automatisch generierter Titel angezeigt.

```csharp
public string Text { get; set; }
```

## Bemerkungen

Verwenden[`Show`](../show/) Option, wenn Sie den Titel ausblenden möchten.

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

* class [ChartTitle](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
