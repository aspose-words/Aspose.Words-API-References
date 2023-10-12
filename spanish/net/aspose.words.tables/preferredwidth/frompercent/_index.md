---
title: PreferredWidth.FromPercent
second_title: Referencia de API de Aspose.Words para .NET
description: PreferredWidth método. Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado como porcentaje.
type: docs
weight: 20
url: /es/net/aspose.words.tables/preferredwidth/frompercent/
---
## PreferredWidth.FromPercent method

Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado como porcentaje.

```csharp
public static PreferredWidth FromPercent(double percent)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| percent | Double | El valor debe ser de 0 a 100. |

### Ejemplos

Muestra cómo configurar una tabla para que se ajuste automáticamente al 50% del ancho de la página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

Muestra cómo establecer un ancho preferido para las celdas de la tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Hay dos formas de aplicar la clase "PreferredWidth" a las celdas de la tabla.
// 1 - Establece un ancho preferido absoluto basado en puntos:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Establece un ancho relativo preferido basado en el porcentaje del ancho de la tabla:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Una celda sin un ancho preferido especificado ocupará el resto del espacio disponible.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Cada configuración de la propiedad "PreferredWidth" crea un nuevo objeto.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Ver también

* class [PreferredWidth](../)
* espacio de nombres [Aspose.Words.Tables](../../preferredwidth/)
* asamblea [Aspose.Words](../../../)


