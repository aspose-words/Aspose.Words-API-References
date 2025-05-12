---
title: ChartMultilevelValue class
linktitle: ChartMultilevelValue class
articleTitle: ChartMultilevelValue class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Charts.ChartMultilevelValue class. Represents a value for charts that display multilevel data."
type: docs
weight: 300
url: /nodejs-net/aspose.words.drawing.charts/chartmultilevelvalue/
---

## ChartMultilevelValue class

Represents a value for charts that display multilevel data.


### Constructors
| Name | Description |
| --- | --- |
| [ChartMultilevelValue(level1, level2, level3)](./constructor/#string_string_string) | Initializes a new instance of this class that represents a three-level value. |
| [ChartMultilevelValue(level1, level2)](./constructor/#string_string) | Initializes a new instance of this class that represents a two-level value. |
| [ChartMultilevelValue(level1)](./constructor/#string) | Initializes a new instance of this class that represents a single-level value. |

### Properties

| Name | Description |
| --- | --- |
| [level1](./level1/) | Gets the name of the chart top level that this value refers to. |
| [level2](./level2/) | Gets the name of the chart intermediate level that this value refers to. |
| [level3](./level3/) | Gets the name of the chart bottom level that this value refers to. |

### Examples

Shows how to create treemap chart.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a Treemap chart.
let shape = builder.insertChart(aw.Drawing.Charts.ChartType.Treemap, 450, 280);
let chart = shape.chart;
chart.title.text = "World Population";

// Delete default generated series.
chart.series.clear();

// Add a series.
let series = chart.series.add(
  "Population by Region",
  [
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "China"),
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "India"),
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "Indonesia"),
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "Pakistan"),
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "Bangladesh"),
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "Japan"),
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "Philippines"),
    new aw.Drawing.Charts.ChartMultilevelValue("Asia", "Other"),
    new aw.Drawing.Charts.ChartMultilevelValue("Africa", "Nigeria"),
    new aw.Drawing.Charts.ChartMultilevelValue("Africa", "Ethiopia"),
    new aw.Drawing.Charts.ChartMultilevelValue("Africa", "Egypt"),
    new aw.Drawing.Charts.ChartMultilevelValue("Africa", "Other"),
    new aw.Drawing.Charts.ChartMultilevelValue("Europe", "Russia"),
    new aw.Drawing.Charts.ChartMultilevelValue("Europe", "Germany"),
    new aw.Drawing.Charts.ChartMultilevelValue("Europe", "Other"),
    new aw.Drawing.Charts.ChartMultilevelValue("Latin America", "Brazil"),
    new aw.Drawing.Charts.ChartMultilevelValue("Latin America", "Mexico"),
    new aw.Drawing.Charts.ChartMultilevelValue("Latin America", "Other"),
    new aw.Drawing.Charts.ChartMultilevelValue("Northern America", "United States", "Other"),
    new aw.Drawing.Charts.ChartMultilevelValue("Northern America", "Other"),
    new aw.Drawing.Charts.ChartMultilevelValue("Oceania")
  ],
  [
    1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
    223800000, 107334000, 105914499, 903000000,
    146150789, 84607016, 516000000,
    203080756, 129713690, 310000000,
    335893238, 35000000,
    42000000
  ]);

// Show data labels.
series.hasDataLabels = true;
series.dataLabels.showValue = true;
series.dataLabels.showCategoryName = true;
let thousandSeparator = ".";
series.dataLabels.numberFormat.formatCode = `#${thousandSeparator}0`;

doc.save(base.artifactsDir + "Charts.treemap.docx");
```

### See Also

* module [Aspose.Words.Drawing.Charts](../)

