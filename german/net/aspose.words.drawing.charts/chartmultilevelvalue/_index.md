---
title: ChartMultilevelValue Class
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.ChartMultilevelValue, um mehrstufige Daten in Ihren Diagrammen effektiv zu verwalten und so Ihre Datenvisualisierungsfunktionen zu verbessern.
type: docs
weight: 1050
url: /de/net/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class

Stellt einen Wert für Diagramme dar, die mehrstufige Daten anzeigen.

```csharp
public class ChartMultilevelValue
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor)(*string*) | Initialisiert eine neue Instanz dieser Klasse, die einen einstufigen Wert darstellt. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_1)(*string, string*) | Initialisiert eine neue Instanz dieser Klasse, die einen zweistufigen Wert darstellt. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_2)(*string, string, string*) | Initialisiert eine neue Instanz dieser Klasse, die einen dreistufigen Wert darstellt. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Level1](../../aspose.words.drawing.charts/chartmultilevelvalue/level1/) { get; } | Ruft den Namen der obersten Diagrammebene ab, auf die sich dieser Wert bezieht. |
| [Level2](../../aspose.words.drawing.charts/chartmultilevelvalue/level2/) { get; } | Ruft den Namen der Diagramm-Zwischenebene ab, auf die sich dieser Wert bezieht. |
| [Level3](../../aspose.words.drawing.charts/chartmultilevelvalue/level3/) { get; } | Ruft den Namen der unteren Diagrammebene ab, auf die sich dieser Wert bezieht. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/chartmultilevelvalue/equals/)(*object*) | Ruft ein Flag ab, das angibt, ob das angegebene Objekt dem aktuellen mehrstufigen Datenobjekt entspricht. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartmultilevelvalue/gethashcode/)() | Ruft einen Hashcode für das aktuelle mehrstufige Datenobjekt ab. |

## Beispiele

Zeigt, wie ein Treemap-Diagramm erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Treemap-Diagramm ein.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Eine Serie hinzufügen.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
