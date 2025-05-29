---
title: ChartNumberFormat.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words för .NET
description: Upptäck hur du använder egenskapen ChartNumberFormat FormatCode för att anpassa dataetikettformat för tydligare insikter och förbättrad datapresentation.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/chartnumberformat/formatcode/
---
## ChartNumberFormat.FormatCode property

Hämtar eller ställer in formatkoden som tillämpas på en dataetikett.

```csharp
public string FormatCode { get; set; }
```

## Anmärkningar

Nummerformatering används för att ändra hur ett värde visas i en dataetikett och kan användas på några mycket kreativa sätt. Exempel på nummerformat:

Nummer - "#,##0.00"

Valuta - "\"$\"#,##0.00"

Tid - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/åååå"

Procentandel - "0,00%"

Bråk - "# ?/?"

Vetenskaplig - "0.00E+00"

Text - "@"

Redovisning - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

Anpassad med färg - "[Röd]-#,##0.0"

## Exempel

Visar hur man ställer in formatering för diagramvärden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie i diagrammet med kategorier för X-axeln,
 // och stora respektive numeriska värden för Y-axeln.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // Ställ in talformatet för Y-axelns tick-etiketter så att siffror inte grupperas med kommatecken.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// Denna flagga kan åsidosätta ovanstående värde och hämta talformatet från källcellen.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

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

* class [ChartNumberFormat](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
