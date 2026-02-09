---
title: ChartMultilevelValue Class
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.ChartMultilevelValue class to effectively manage multilevel data in your charts, enhancing your data visualization capabilities.
type: docs
weight: 1050
url: /net/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class

Represents a value for charts that display multilevel data.

```csharp
public class ChartMultilevelValue
```

## Constructors

| Name | Description |
| --- | --- |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor)(*string*) | Initializes a new instance of this class that represents a single-level value. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_1)(*string, string*) | Initializes a new instance of this class that represents a two-level value. |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_2)(*string, string, string*) | Initializes a new instance of this class that represents a three-level value. |

## Properties

| Name | Description |
| --- | --- |
| [Level1](../../aspose.words.drawing.charts/chartmultilevelvalue/level1/) { get; } | Gets the name of the chart top level that this value refers to. |
| [Level2](../../aspose.words.drawing.charts/chartmultilevelvalue/level2/) { get; } | Gets the name of the chart intermediate level that this value refers to. |
| [Level3](../../aspose.words.drawing.charts/chartmultilevelvalue/level3/) { get; } | Gets the name of the chart bottom level that this value refers to. |

## Methods

| Name | Description |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/chartmultilevelvalue/equals/)(*object*) | Gets a flag indicating whether the specified object is equal to the current multilevel data object. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartmultilevelvalue/gethashcode/)() | Gets a hash code for the current multilevel data object. |

## Examples

Shows how to create treemap chart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a Treemap chart.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Delete default generated series.
chart.Series.Clear();

// Add a series.
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

// Show data labels.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
