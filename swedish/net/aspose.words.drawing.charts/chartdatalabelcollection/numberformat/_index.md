---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartDataLabelCollection NumberFormat för att enkelt anpassa dataetikettformat för hela din serie, vilket förbättrar tydlighet och presentation.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Får en[`ChartNumberFormat`](../../chartnumberformat/) instans som tillåter att ställa in talformat för dataetiketterna för hela serien .

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## Exempel

Visar hur man aktiverar och konfigurerar dataetiketter för en diagramserie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till ett linjediagram och rensa sedan dess demodataserie för att börja med ett rent diagram,
// och ange sedan en titel.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Infoga en anpassad diagramserie med månader som kategorier för X-axeln,
// och respektive decimalbelopp för Y-axeln.
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// Aktivera dataetiketter och använd sedan ett anpassat talformat för värden som visas i dataetiketterna.
// Detta format behandlar visade decimalvärden som miljoner amerikanska dollar.
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
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
