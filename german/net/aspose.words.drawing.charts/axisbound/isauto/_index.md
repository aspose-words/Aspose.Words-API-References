---
title: AxisBound.IsAuto
second_title: Aspose.Words für .NET-API-Referenz
description: AxisBound eigendom. Gibt ein Flag zurück das angibt dass die Achsengrenze automatisch bestimmt werden soll.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/axisbound/isauto/
---
## AxisBound.IsAuto property

Gibt ein Flag zurück, das angibt, dass die Achsengrenze automatisch bestimmt werden soll.

```csharp
public bool IsAuto { get; }
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

// Eine Reihe mit zwei Dezimalarrays hinzufügen. Das erste Array enthält die X-Werte,
// und der zweite enthält entsprechende Y-Werte für Punkte im Streudiagramm.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// Standardmäßig wird die Standardskalierung auf die X- und Y-Achsen des Diagramms angewendet.
// sodass beide Bereiche groß genug sind, um jeden X- und Y-Wert jeder Reihe zu umfassen.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Wir können unsere eigenen Achsengrenzen definieren.
// In diesem Fall stellen wir sicher, dass sowohl die X- als auch die Y-Achsenlineale einen Bereich von 0 bis 10 anzeigen.
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

// Wir können Achsengrenzen auch in Form von Datumsangaben festlegen und so das Diagramm auf einen Zeitraum beschränken.
// Wenn Sie den Bereich auf 1980-1990 festlegen, werden die beiden Serienwerte weggelassen
// die außerhalb des Bereichs des Diagramms liegen.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Siehe auch

* class [AxisBound](../)
* namensraum [Aspose.Words.Drawing.Charts](../../axisbound/)
* Montage [Aspose.Words](../../../)


