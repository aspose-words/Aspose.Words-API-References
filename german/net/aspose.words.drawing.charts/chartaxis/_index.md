---
title: Class ChartAxis
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartAxis klas. Stellt die Achsenoptionen des Diagramms dar.
type: docs
weight: 630
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
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob die Wertachse die Kategorieachse zwischen Kategorien kreuzt. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Gibt die kleinste Zeiteinheit zurück, die auf der Zeitkategorieachse dargestellt wird, oder legt sie fest. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Ruft den Typ der Kategorieachse ab oder legt diesen fest. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Gibt an, wie diese Achse die senkrechte Achse schneidet. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Gibt an, wo sich die Achse auf der senkrechten Achse kreuzt. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Gibt den Skalierungswert der Anzeigeeinheiten für die Werteachse an. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Gibt das Dokument zurück, zu dem der Titelinhaber gehört. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob die Achse über Hauptgitterlinien verfügt. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob die Achse Nebengitterlinien hat. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob diese Achse ausgeblendet ist oder nicht. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Gibt die wichtigsten Teilstriche zurück oder setzt sie. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Gibt den Abstand zwischen den Hauptteilstrichen zurück oder legt ihn fest. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob der Standardabstand zwischen den Hauptteilstrichen verwendet werden soll. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Gibt den Skalenwert für Hauptteilstriche auf der Zeitkategorieachse zurück oder legt diesen fest. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Gibt die kleinen Teilstriche für die Achse zurück oder setzt sie. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Gibt den Abstand zwischen kleinen Teilstrichen zurück oder legt ihn fest. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob der Standardabstand zwischen kleinen Teilstrichen verwendet werden soll. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Gibt den Skalenwert für kleine Teilstriche auf der Zeitkategorieachse zurück oder legt diesen fest. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Gibt a zurück[`ChartNumberFormat`](../chartnumberformat/) Objekt, das die Definition von Zahlenformaten für die Achse ermöglicht. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Gibt ein Flag zurück oder setzt es, das angibt, ob die Werte der Achse in umgekehrter Reihenfolge angezeigt werden sollen, d. h. von max nach min. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Bietet Zugriff auf die Skalierungsoptionen der Achse. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment/) { get; set; } | Ruft die Textausrichtung von Achsenteilstrichbeschriftungen ab oder legt diese fest. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset/) { get; set; } | Ruft den Abstand der Beschriftungen von der Achse ab oder legt diesen fest. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition/) { get; set; } | Gibt die Position der Teilstrichbeschriftungen auf der Achse zurück oder legt sie fest. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing/) { get; set; } | Ruft das Intervall ab, in dem Teilstrichbeschriftungen gezeichnet werden, oder legt dieses fest. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob das automatische Intervall zum Zeichnen von Teilstrichbeschriftungen verwendet werden soll. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Ruft das Intervall ab, in dem Teilstriche gezeichnet werden, oder legt es fest. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Bietet Zugriff auf die Eigenschaften des Achsentitels. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Gibt den Typ der Achse zurück. |

### Beispiele

Zeigt, wie man ein Diagramm einfügt und das Erscheinungsbild seiner Achsen ändert.

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
// wie ihre Richtung, Dur-/Moll-Einheitenstriche und Teilstriche.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Säulendiagramme haben keine Z-Achse.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


