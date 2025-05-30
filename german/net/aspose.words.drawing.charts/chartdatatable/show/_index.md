---
title: ChartDataTable.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words für .NET
description: Steuern Sie die Sichtbarkeit Ihres Diagramms mit der Eigenschaft „ChartDataTable Show“. Schalten Sie die Datentabellenanzeige einfach um, um bessere Einblicke in die Daten zu erhalten. Standard „false“.
type: docs
weight: 70
url: /de/net/aspose.words.drawing.charts/chartdatatable/show/
---
## ChartDataTable.Show property

Ruft ein Flag ab oder legt es fest, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. Der Standardwert ist`FALSCH` .

```csharp
public bool Show { get; set; }
```

## Bemerkungen

Die folgenden Diagrammtypen unterstützen keine Datentabellen: Streudiagramm, Kreisdiagramm, Ringdiagramm, Oberflächendiagramm, Radardiagramm, Treemap-Diagramm, Sunburst-Diagramm, Histogramm-Diagramm, Pareto-Diagramm, Box-and-Whisker-Diagramm, Wasserfall-Diagramm, Trichter-Diagramm und Kombinationsdiagramme, die Reihen dieser Typen enthalten. Das Anzeigen einer Datentabelle für diese Diagrammtypen führt zu einemInvalidOperationException Ausnahme.

## Beispiele

Zeigt, wie eine Datentabelle mit Diagrammreihendaten angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Siehe auch

* class [ChartDataTable](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
