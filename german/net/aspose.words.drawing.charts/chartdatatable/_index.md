---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartDataTable, um Diagrammdatentabellen einfach anzupassen und Ihre Datenvisualisierung mit leistungsstarken Funktionen zu verbessern.
type: docs
weight: 990
url: /de/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Ermöglicht die Angabe von Eigenschaften einer Diagrammdatentabelle.

```csharp
public class ChartDataTable
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Bietet Zugriff auf die Schriftformatierung der Datentabelle. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Bietet Zugriff auf die Füllung des Texthintergrunds und die Rahmenformatierung der Datentabelle. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob ein horizontaler Rahmen der Datentabelle angezeigt wird. Der Standardwert ist`WAHR` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob Legendenschlüssel in der Datentabelle angezeigt werden. Der Standardwert ist`WAHR` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Ruft ein Flag ab oder setzt es, das angibt, ob ein Rahmen, d. h. ein Rahmen um Serien- und Kategorienamen, angezeigt wird. Der Standardwert ist`WAHR` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob ein vertikaler Rahmen der Datentabelle angezeigt wird. Der Standardwert ist`WAHR` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. Der Standardwert ist`FALSCH` . |

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
