---
title: AxisBound.ValueAsDate
linktitle: ValueAsDate
articleTitle: ValueAsDate
second_title: Aspose.Words för .NET
description: Upptäck egenskapen AxisBound ValueAsDate, som effektivt returnerar axelbundna värden som datum och tid för förbättrad datavisualisering och analys.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/axisbound/valueasdate/
---
## AxisBound.ValueAsDate property

Returnerar värdet för axelgränsen representerad som datetime.

```csharp
public DateTime ValueAsDate { get; }
```

## Exempel

Visar hur man ställer in anpassade axelgränser.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en serie med två decimalmatriser. Den första matrisen innehåller X-värdena,
// och den andra innehåller motsvarande Y-värden för punkter i punktdiagrammet.
chart.Series.Add("Series 1",
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 },
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Som standard tillämpas standardskalning på grafens X- och Y-axlar,
// så att båda deras intervall är tillräckligt stora för att omfatta varje X- och Y-värde i varje serie.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Vi kan definiera våra egna axelgränser.
// I det här fallet kommer vi att visa ett intervall från 0 till 10 på både X- och Y-axelns linjaler.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Skapa ett linjediagram med en serie som kräver ett datumintervall på X-axeln och decimalvärden för Y-axeln.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// Vi kan också sätta axelgränser i form av datum, vilket begränsar diagrammet till en period.
// Om intervallet sätts till 1980-1990 utelämnas de två serievärdena
// som ligger utanför intervallet från grafen.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Se även

* class [AxisBound](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
