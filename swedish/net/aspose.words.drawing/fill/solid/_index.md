---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words för .NET
description: Upptäck Fill Solid-metoden för att uppnå en enhetlig färgfyllning, vilket enkelt förbättrar din designs visuella attraktionskraft och enhetlighet.
type: docs
weight: 260
url: /sv/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Ställer in fyllningen till en enhetlig färg.

```csharp
public void Solid()
```

## Anmärkningar

Använd den här metoden för att konvertera vilken som helst av fyllningarna tillbaka till heldragen fyllning.

## Exempel

Visar hur man konverterar tillbaka fyllningarna till heldragen fyllning.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Hämta Fill-objekt för teckensnittet för den första körningen.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Kontrollera fyllningsegenskaperna för teckensnittet.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Ändra fyllningstyp till Helfärgad med enhetlig grön färg.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Ställer in fyllningen till en angiven enhetlig färg.

```csharp
public void Solid(Color color)
```

## Anmärkningar

Använd den här metoden för att konvertera vilken som helst av fyllningarna tillbaka till heldragen fyllning.

## Exempel

Visar hur man använder diagramformatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Radera serier som genereras som standard.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formatera diagrambakgrund.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Dölj axeltackningsetiketter.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formatera diagramtitel.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatera axeltitel.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatförklaring.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
