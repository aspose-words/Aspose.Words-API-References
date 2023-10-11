---
title: ChartTitle.Text
second_title: Aspose.Words für .NET-API-Referenz
description: ChartTitle eigendom. Ruft den Text des Diagrammtitels ab oder legt ihn fest. WennNull oder ein leerer Wert angegeben wird wird der automatisch generierte Titel angezeigt.
type: docs
weight: 40
url: /de/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

Ruft den Text des Diagrammtitels ab oder legt ihn fest. Wenn`Null` oder ein leerer Wert angegeben wird, wird der automatisch generierte Titel angezeigt.

```csharp
public string Text { get; set; }
```

### Bemerkungen

Verwenden[`Show`](../show/) Option, wenn Sie den Titel ausblenden müssen.

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

* class [ChartTitle](../)
* namensraum [Aspose.Words.Drawing.Charts](../../charttitle/)
* Montage [Aspose.Words](../../../)


