---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words für .NET
description: Entdecken Sie die Fill Solid-Methode zum Erreichen einer konsistenten Farbfüllung und verbessern Sie mühelos die visuelle Attraktivität und Einheitlichkeit Ihres Designs.
type: docs
weight: 260
url: /de/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Legt die Füllung auf eine einheitliche Farbe fest.

```csharp
public void Solid()
```

## Bemerkungen

Verwenden Sie diese Methode, um alle Füllungen wieder in Vollfüllungen umzuwandeln.

## Beispiele

Zeigt, wie Sie beliebige Füllungen wieder in Vollfüllungen umwandeln.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Füllobjekt für die Schriftart des ersten Laufs abrufen.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Fülleigenschaften der Schriftart prüfen.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Ändern Sie den Füllungstyp in „Einfarbig“ mit einheitlicher grüner Farbe.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Legt die Füllung auf eine angegebene einheitliche Farbe fest.

```csharp
public void Solid(Color color)
```

## Bemerkungen

Verwenden Sie diese Methode, um alle Füllungen wieder in Vollfüllungen umzuwandeln.

## Beispiele

Zeigt, wie die Diagrammformatierung verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Diagrammhintergrund formatieren.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Achsenmarkierungsbeschriftungen ausblenden.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Diagrammtitel formatieren.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Achsentitel formatieren.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Legende formatieren.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Siehe auch

* class [Fill](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
