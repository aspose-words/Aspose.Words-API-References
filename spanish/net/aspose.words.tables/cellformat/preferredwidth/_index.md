---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words para .NET
description: CellFormat PreferredWidth propiedad. Devuelve o establece el ancho preferido de la celda en C#.
type: docs
weight: 70
url: /es/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Devuelve o establece el ancho preferido de la celda.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Observaciones

El ancho preferido (junto con la opción Ajuste automático de la tabla) determina cómo el algoritmo de diseño de la tabla calcula el ancho real de la celda. El diseño de la tabla se puede realizar mediante Aspose.Words cuando guarda el documento o mediante Microsoft Word cuando muestra el documento.

El ancho preferido se puede especificar en puntos o en porcentaje. El ancho preferido también se puede especificar como "auto", lo que significa que no se especifica ningún ancho preferido.

El valor predeterminado es[`Auto`](../../preferredwidth/auto/).

## Ejemplos

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
