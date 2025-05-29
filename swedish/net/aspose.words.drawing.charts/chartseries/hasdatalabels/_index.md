---
title: ChartSeries.HasDataLabels
linktitle: HasDataLabels
articleTitle: HasDataLabels
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartSeries HasDataLabels för att enkelt hantera synligheten av dataetiketter för dina serier och förbättra din datavisualiseringsupplevelse.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing.charts/chartseries/hasdatalabels/
---
## ChartSeries.HasDataLabels property

Hämtar eller ställer in en flagga som anger om dataetiketter visas för serien.

```csharp
public bool HasDataLabels { get; set; }
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

* class [ChartSeries](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
