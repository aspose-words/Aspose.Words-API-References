---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words för .NET
description: ChartDataLabelCollection Font fast egendom. Ger tillgång till teckensnittsformateringen av dataetiketterna för hela serien i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

Ger tillgång till teckensnittsformateringen av dataetiketterna för hela serien.

```csharp
public Font Font { get; }
```

## Anmärkningar

Värdet som definierats för den här egenskapen kan åsidosättas för en individuell dataetikett med hjälp av [`Font`](../../chartdatalabel/font/) egenskap.

## Exempel

Visar hur du aktiverar och konfigurerar dataetiketter för en diagramserie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till ett linjediagram, rensa sedan dess demodataserie för att börja med ett rent diagram,
// och ställ sedan in en titel.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Infoga en anpassad diagramserie med månader som kategorier för X-axeln,
// och respektive decimaltal för Y-axeln.
ChartSeries series = chart.Series.Add("Revenue", 
    new[] { "January", "February", "March" }, 
    new[] { 25.611d, 21.439d, 33.750d });

// Aktivera dataetiketter och använd sedan ett anpassat talformat för värden som visas i dataetiketterna.
// Detta format kommer att behandla visade decimalvärden som miljoner amerikanska dollar.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;            

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### Se även

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
