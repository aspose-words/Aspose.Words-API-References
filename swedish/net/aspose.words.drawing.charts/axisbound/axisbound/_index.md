---
title: AxisBound
linktitle: AxisBound
articleTitle: AxisBound
second_title: Aspose.Words för .NET
description: Skapa enkelt dynamiska axelgränser med AxisBound-konstruktorn, vilket gör att ditt ordbehandlingsprogram automatiskt kan bestämma optimala layouter för en förbättrad användarupplevelse.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound() {#constructor}

Skapar en ny instans som anger att axelgränsen ska bestämmas automatiskt av ett ordbehandlingsprogram.

```csharp
public AxisBound()
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

---

## AxisBound(*double*) {#constructor_1}

Skapar en axelgräns representerad som ett tal.

```csharp
public AxisBound(double value)
```

## Exempel

Visar hur man infogar ett diagram med datum-/tidsvärden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie som innehåller datum-/tidsvärden för X-axeln och respektive decimalvärden för Y-axeln.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Ange nedre och övre gränser för X-axeln.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Ställ in de större enheterna på X-axeln till en vecka och de mindre enheterna till en dag.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Definiera Y-axelegenskaper för decimalvärden.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Se även

* class [AxisBound](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)

---

## AxisBound(*DateTime*) {#constructor_2}

Skapar en axelgräns representerad som ett datum- och tidsvärde.

```csharp
public AxisBound(DateTime datetime)
```

## Exempel

Visar hur man infogar ett diagram med datum-/tidsvärden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Rensa diagrammets demodataserie för att börja med ett rent diagram.
chart.Series.Clear();

// Lägg till en anpassad serie som innehåller datum-/tidsvärden för X-axeln och respektive decimalvärden för Y-axeln.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Ange nedre och övre gränser för X-axeln.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Ställ in de större enheterna på X-axeln till en vecka och de mindre enheterna till en dag.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Definiera Y-axelegenskaper för decimalvärden.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Se även

* class [AxisBound](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
