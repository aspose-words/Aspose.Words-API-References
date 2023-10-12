---
title: Class AxisBound
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.AxisBound klas. Stellt die minimale oder maximale Grenze der Achsenwerte dar.
type: docs
weight: 510
url: /de/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Stellt die minimale oder maximale Grenze der Achsenwerte dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public sealed class AxisBound
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Erstellt eine neue Instanz, die angibt, dass die Achsengrenze automatisch von einer Textverarbeitungsanwendung bestimmt werden soll. |
| [AxisBound](axisbound/#constructor_2)(DateTime) | Erstellt eine Achsengrenze, die als Datum/Uhrzeit-Wert dargestellt wird. |
| [AxisBound](axisbound/#constructor_1)(double) | Erstellt eine als Zahl dargestellte Achsengrenze. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Gibt ein Flag zurück, das angibt, dass die Achsengrenze automatisch bestimmt werden soll. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Gibt den numerischen Wert der Achsengrenze zurück. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Gibt den Wert der Achsengrenze zurück, dargestellt als Datum/Uhrzeit. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(object) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Dient als Hash-Funktion für diesen Typ. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Gibt eine benutzerfreundliche Zeichenfolge zurück, die den Wert dieses Objekts anzeigt. |

### Bemerkungen

Bound kann als numerischer Wert, Datum/Uhrzeit-Wert oder spezieller „Auto“-Wert angegeben werden.

Die Instanzen dieser Klasse sind unveränderlich.

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

// Untere und obere Grenze für die X-Achse festlegen.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Setze die Haupteinheiten der X-Achse auf eine Woche und die Nebeneinheiten auf einen Tag.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Y-Achsen-Eigenschaften für Dezimalwerte definieren.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


