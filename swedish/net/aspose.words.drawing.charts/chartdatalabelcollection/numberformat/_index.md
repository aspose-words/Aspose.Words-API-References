---
title: ChartDataLabelCollection.NumberFormat
second_title: Aspose.Words för .NET API Referens
description: ChartDataLabelCollection fast egendom. Får enChartNumberFormat instans som gör det möjligt att ställa in nummerformat för dataetiketterna för hela serien.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Får en[`ChartNumberFormat`](../../chartnumberformat/) instans som gör det möjligt att ställa in nummerformat för dataetiketterna för hela serien.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### Exempel

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* hopsättning [Aspose.Words](../../../)


