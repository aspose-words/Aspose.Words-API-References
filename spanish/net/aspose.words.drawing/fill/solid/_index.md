---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words para .NET
description: Descubra el método Relleno sólido para lograr un relleno de color consistente, mejorando el atractivo visual y la uniformidad de su diseño sin esfuerzo.
type: docs
weight: 260
url: /es/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Establece el relleno en un color uniforme.

```csharp
public void Solid()
```

## Observaciones

Utilice este método para convertir cualquiera de los rellenos nuevamente en relleno sólido.

## Ejemplos

Muestra cómo convertir cualquiera de los rellenos nuevamente a relleno sólido.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Obtener el objeto de relleno para la fuente de la primera ejecución.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Verificar las propiedades de relleno de la fuente.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Cambia el tipo de relleno a Sólido con color verde uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Establece el relleno en un color uniforme especificado.

```csharp
public void Solid(Color color)
```

## Observaciones

Utilice este método para convertir cualquiera de los rellenos nuevamente en relleno sólido.

## Ejemplos

Muestra cómo utilizar el formato de gráficos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

//Eliminar serie generada por defecto.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formatear el fondo del gráfico.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Ocultar las etiquetas de las marcas de los ejes.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formatear el título del gráfico.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

//Formatear título del eje.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formato de leyenda.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Ver también

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
