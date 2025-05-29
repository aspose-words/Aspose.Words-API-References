---
title: ChartAxis Class
linktitle: ChartAxis
articleTitle: ChartAxis
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartAxis für anpassbare Diagrammachsenoptionen. Verbessern Sie Ihre Datenvisualisierung mühelos!
type: docs
weight: 890
url: /de/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Stellt die Achsenoptionen des Diagramms dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartAxis
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob die Werteachse die Kategorieachse zwischen Kategorien schneidet. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Gibt die kleinste Zeiteinheit zurück, die auf der Zeitkategorieachse dargestellt wird, oder legt sie fest. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Ruft den Typ der Kategorieachse ab oder legt ihn fest. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Gibt an, wie diese Achse die senkrechte Achse schneidet. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Gibt an, wo auf der senkrechten Achse die Achse kreuzt. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Gibt den Skalierungswert der Anzeigeeinheiten für die Werteachse an. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Gibt das Dokument zurück, das das übergeordnete Diagramm enthält. |
| [Format](../../aspose.words.drawing.charts/chartaxis/format/) { get; } | Bietet Zugriff auf die Linienformatierung der Achse und die Füllung der Teilstrichbeschriftungen. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob die Achse über Hauptgitternetzlinien verfügt. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob die Achse über Nebengitternetzlinien verfügt. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob diese Achse ausgeblendet ist oder nicht. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Gibt die Hauptmarkierungen zurück oder legt sie fest. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Gibt den Abstand zwischen den Hauptmarkierungen zurück oder legt ihn fest. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob der Standardabstand zwischen den Hauptmarkierungen verwendet werden soll. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Gibt den Skalenwert für die Hauptmarkierungen auf der Zeitkategorieachse zurück oder legt ihn fest. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Gibt die kleinen Teilstriche für die Achse zurück oder legt sie fest. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Gibt den Abstand zwischen kleineren Teilstrichen zurück oder legt ihn fest. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob der Standardabstand zwischen kleinen Teilstrichen verwendet werden soll. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Gibt den Skalierungswert für kleinere Teilstriche auf der Zeitkategorieachse zurück oder legt ihn fest. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Gibt einen[`ChartNumberFormat`](../chartnumberformat/) Objekt, mit dem Zahlenformate für die Achse definiert werden können. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Gibt ein Flag zurück oder setzt es, das angibt, ob die Werte der Achse in umgekehrter Reihenfolge angezeigt werden sollen, d. h. von Maximum bis Minimum. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Bietet Zugriff auf die Skalierungsoptionen der Achse. |
| [TickLabels](../../aspose.words.drawing.charts/chartaxis/ticklabels/) { get; } | Bietet Zugriff auf die Eigenschaften der Beschriftungen der Achsenmarkierungen. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Ruft das Intervall ab oder legt es fest, in dem Teilstriche gezeichnet werden. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Bietet Zugriff auf die Achsentiteleigenschaften. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Gibt den Typ der Achse zurück. |

## Beispiele

Zeigt, wie Sie ein Diagramm einfügen und die Darstellung seiner Achsen ändern.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine Diagrammreihe mit Kategorien für die X-Achse und entsprechenden numerischen Werten für die Y-Achse ein.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Diagrammachsen haben verschiedene Optionen, die ihr Aussehen ändern können,
// wie etwa ihre Richtung, große/kleine Einheitsstriche und Teilstriche.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Säulendiagramme haben keine Z-Achse.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
