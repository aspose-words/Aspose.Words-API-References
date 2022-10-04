---
title: AxisBound
second_title: Aspose.Words für .NET-API-Referenz
description: Erstellt eine neue Instanz die angibt dass die Achsenbegrenzung automatisch von einer Textverarbeitungsanwendung bestimmt werden soll.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound() {#constructor}

Erstellt eine neue Instanz, die angibt, dass die Achsenbegrenzung automatisch von einer Textverarbeitungsanwendung bestimmt werden soll.

```csharp
public AxisBound()
```

### Beispiele

Zeigt, wie benutzerdefinierte Achsengrenzen festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Füge eine Reihe mit zwei Dezimalarrays hinzu. Das erste Array enthält die X-Werte,
// und die zweite enthält entsprechende Y-Werte für Punkte im Streudiagramm.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Standardmäßig wird die Standard-Skalierung auf die X- und Y-Achsen des Diagramms angewendet,
// so dass beide Bereiche groß genug sind, um jeden X- und Y-Wert jeder Serie zu umfassen.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Wir können unsere eigenen Achsengrenzen definieren.
// In diesem Fall lassen wir sowohl das X- als auch das Y-Achsenlineal einen Bereich von 0 bis 10 anzeigen.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Erstellen Sie ein Liniendiagramm mit einer Reihe, die einen Datumsbereich auf der X-Achse und Dezimalwerte für die Y-Achse erfordert.
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

// Wir können auch Achsengrenzen in Form von Datumsangaben festlegen, wodurch das Diagramm auf einen Zeitraum begrenzt wird.
// Wenn Sie den Bereich auf 1980-1990 setzen, werden die beiden Serienwerte weggelassen
// die außerhalb des Bereichs des Diagramms liegen.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Siehe auch

* class [AxisBound](../)
* namensraum [Aspose.Words.Drawing.Charts](../../axisbound/)
* Montage [Aspose.Words](../../../)

---

## AxisBound(double) {#constructor_1}

Erstellt eine als Zahl dargestellte Achsengrenze.

```csharp
public AxisBound(double value)
```

### Beispiele

Zeigt, wie ein Diagramm mit Datums-/Uhrzeitwerten eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine benutzerdefinierte Reihe hinzu, die Datums-/Uhrzeitwerte für die X-Achse und entsprechende Dezimalwerte für die Y-Achse enthält.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Untere und obere Grenzen für die X-Achse setzen.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Setze die Haupteinheiten der X-Achse auf eine Woche und die Nebeneinheiten auf einen Tag.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Eigenschaften der Y-Achse für Dezimalwerte definieren.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Siehe auch

* class [AxisBound](../)
* namensraum [Aspose.Words.Drawing.Charts](../../axisbound/)
* Montage [Aspose.Words](../../../)

---

## AxisBound(DateTime) {#constructor_2}

Erstellt eine Achsengrenze, die als datetime-Wert dargestellt wird.

```csharp
public AxisBound(DateTime datetime)
```

### Beispiele

Zeigt, wie ein Diagramm mit Datums-/Uhrzeitwerten eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem sauberen Diagramm zu beginnen.
chart.Series.Clear();

// Fügen Sie eine benutzerdefinierte Reihe hinzu, die Datums-/Uhrzeitwerte für die X-Achse und entsprechende Dezimalwerte für die Y-Achse enthält.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Untere und obere Grenzen für die X-Achse setzen.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Setze die Haupteinheiten der X-Achse auf eine Woche und die Nebeneinheiten auf einen Tag.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Eigenschaften der Y-Achse für Dezimalwerte definieren.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Siehe auch

* class [AxisBound](../)
* namensraum [Aspose.Words.Drawing.Charts](../../axisbound/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
