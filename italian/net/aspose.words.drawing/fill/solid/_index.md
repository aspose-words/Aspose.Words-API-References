---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words per .NET
description: Scopri il metodo Riempimento continuo per ottenere un riempimento di colore uniforme, migliorando senza sforzo l'aspetto visivo e l'uniformità del tuo progetto.
type: docs
weight: 260
url: /it/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Imposta il riempimento su un colore uniforme.

```csharp
public void Solid()
```

## Osservazioni

Utilizzare questo metodo per convertire uno qualsiasi dei riempimenti in riempimento pieno.

## Esempi

Mostra come riconvertire uno qualsiasi dei riempimenti in riempimento uniforme.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Ottieni l'oggetto Fill per il font della prima esecuzione.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Controlla le proprietà di riempimento del font.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Cambia il tipo di riempimento in Solido con colore verde uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Imposta il riempimento su un colore uniforme specificato.

```csharp
public void Solid(Color color)
```

## Osservazioni

Utilizzare questo metodo per convertire uno qualsiasi dei riempimenti in riempimento pieno.

## Esempi

Mostra come utilizzare la formattazione dei grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Elimina le serie generate di default.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formatta lo sfondo del grafico.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Nascondi le etichette delle tacche degli assi.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formatta il titolo del grafico.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatta il titolo dell'asse.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatta la legenda.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
