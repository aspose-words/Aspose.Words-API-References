---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.AxisBound, din lösning för att definiera axelvärdesgränser i diagram för exakt datavisualisering.
type: docs
weight: 750
url: /sv/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Representerar den minsta eller största gränsen för axelvärden.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public sealed class AxisBound
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Skapar en ny instans som anger att axelgränsen ska bestämmas automatiskt av ett ordbehandlingsprogram. |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | Skapar en axelgräns representerad som ett datum- och tidsvärde. |
| [AxisBound](axisbound/#constructor_1)(*double*) | Skapar en axelgräns representerad som ett tal. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Returnerar en flagga som anger att axelgränsen ska bestämmas automatiskt. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Returnerar det numeriska värdet för axelns gräns. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Returnerar värdet för axelgränsen representerad som datetime. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Fungerar som en hashfunktion för den här typen. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Returnerar en användarvänlig sträng som visar värdet för detta objekt. |

## Anmärkningar

Bound kan anges som ett numeriskt värde, ett datum- och tidsvärde eller ett speciellt "auto"-värde.

Instanserna av den här klassen är oföränderliga.

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
