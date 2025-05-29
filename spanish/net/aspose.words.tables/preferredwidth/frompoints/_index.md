---
title: PreferredWidth.FromPoints
linktitle: FromPoints
articleTitle: FromPoints
second_title: Aspose.Words para .NET
description: Descubra el método PreferredWidth FromPoints para crear una nueva instancia con un ancho definido en puntos, mejorando la precisión y la eficiencia de su diseño.
type: docs
weight: 30
url: /es/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado utilizando una cantidad de puntos.

```csharp
public static PreferredWidth FromPoints(double points)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| points | Double | El valor debe ser de 0 a 22 pulgadas (22 * 72 puntos). |

## Ejemplos

Muestra cómo utilizar herramientas de conversión de unidades al especificar un ancho preferido para una celda.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(ConvertUtil.InchToPoint(3));
builder.InsertCell();

Assert.AreEqual(216.0d, table.FirstRow.FirstCell.CellFormat.PreferredWidth.Value);
```

Muestra cómo establecer un ancho preferido para las celdas de la tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Hay dos formas de aplicar la clase "PreferredWidth" a las celdas de la tabla.
// 1 - Establezca un ancho preferido absoluto basado en puntos:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Establezca un ancho relativo preferido basado en el porcentaje del ancho de la tabla:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Una celda sin un ancho preferido especificado ocupará el resto del espacio disponible.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

//Cada configuración de la propiedad "PreferredWidth" crea un nuevo objeto.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Ver también

* class [PreferredWidth](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
