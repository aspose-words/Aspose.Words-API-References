---
title: Enum ChartType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.Charts.ChartType uppräkning. Anger typen av ett diagram.
type: docs
weight: 830
url: /sv/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Anger typen av ett diagram.

```csharp
public enum ChartType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Area | `0` | Ytdiagram. |
| AreaStacked | `1` | Stacked area diagram. |
| AreaPercentStacked | `2` | 100 % staplade ytdiagram. |
| Area3D | `3` | 3D Ytdiagram. |
| Area3DStacked | `4` | 3D Stacked Area diagram. |
| Area3DPercentStacked | `5` | 3D 100 % staplade områdesdiagram. |
| Bar | `6` | Stapeldiagram. |
| BarStacked | `7` | Staplade stapeldiagram. |
| BarPercentStacked | `8` | 100 % staplat stapeldiagram. |
| Bar3D | `9` | 3D stapeldiagram. |
| Bar3DStacked | `10` | 3D staplade stapeldiagram. |
| Bar3DPercentStacked | `11` | 3D 100 % staplade stapeldiagram. |
| Bubble | `12` | Bubbeldiagram. |
| Bubble3D | `13` | 3D bubbeldiagram. |
| Column | `14` | Kolumndiagram. |
| ColumnStacked | `15` | Staplade kolumndiagram. |
| ColumnPercentStacked | `16` | 100 % staplade kolumndiagram. |
| Column3D | `17` | 3D-kolumndiagram. |
| Column3DStacked | `18` | 3D staplade kolumndiagram. |
| Column3DPercentStacked | `19` | 3D 100 % staplade kolumndiagram. |
| Column3DClustered | `20` | 3D-klustrade kolumndiagram. |
| Doughnut | `21` | Donut diagram. |
| Line | `22` | Linjediagram. |
| LineStacked | `23` | Staplade linjediagram. |
| LinePercentStacked | `24` | 100 % staplade linjediagram. |
| Line3D | `25` | 3D-linjediagram. |
| Pie | `26` | Cirkeldiagram. |
| Pie3D | `27` | 3D-cirkeldiagram. |
| PieOfBar | `28` | Stapeldiagram. |
| PieOfPie | `29` | Cirkeldiagram. |
| Radar | `30` | Radardiagram. |
| Scatter | `31` | Spridningsdiagram. |
| Stock | `32` | Aktiediagram. |
| Surface | `33` | Ytdiagram. |
| Surface3D | `34` | 3D Ytdiagram. |

### Exempel

Visar hur man skapar en lämplig typ av diagramserie för en graftyp.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Det finns flera sätt att fylla i ett diagrams seriesamling.
    // Olika seriescheman är avsedda för olika diagramtyper.
    // 1 - Kolumndiagram med kolumner grupperade och bandade längs X-axeln efter kategori:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Infoga två serier av decimalvärden som innehåller ett värde för varje respektive kategori.
    // Detta kolumndiagram kommer att ha tre grupper, var och en med två kolumner.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Kategorier är fördelade längs X-axeln, och värden är fördelade längs Y-axeln.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Ytdiagram med datum fördelade längs X-axeln:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Infoga en serie med ett decimalvärde för respektive datum.
    // Datumen kommer att fördelas längs en linjär X-axel,
    // och värdena som läggs till i denna serie kommer att skapa datapunkter.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D spridningsdiagram:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Varje serie kommer att behöva två decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden och den andra innehåller motsvarande Y-värden
    // av datapunkter på diagrammets graf.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Bubbeldiagram:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Varje serie kommer att behöva tre decimalmatriser av samma längd.
    // Den första matrisen innehåller X-värden, den andra innehåller motsvarande Y-värden,
    // och den tredje innehåller diametrar för var och en av grafens datapunkter.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Infoga ett diagram med hjälp av en dokumentbyggare med en specificerad diagramtyp, bredd och höjd, och ta bort dess demodata.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)


