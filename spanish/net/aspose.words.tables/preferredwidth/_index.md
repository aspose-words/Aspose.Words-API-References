---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Tables.PreferredWidth, su solución para definir anchos óptimos de tablas y celdas con precisión y flexibilidad. ¡Mejore el diseño de sus documentos hoy mismo!
type: docs
weight: 7140
url: /es/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Representa un valor y su unidad de medida que se utiliza para especificar el ancho preferido de una tabla o una celda.

Para obtener más información, visite el[Trabajar con tablas](https://docs.aspose.com/words/net/working-with-tables/) Artículo de documentación.

```csharp
public sealed class PreferredWidth
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Obtiene la unidad de medida utilizada para este valor de ancho preferido. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Obtiene el valor de ancho preferido. La unidad de medida se especifica en el[`Type`](./type/) propiedad. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado como un porcentaje. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado utilizando una cantidad de puntos. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Determina si el objeto especificado es igual en valor al objeto actual. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Determina si el especificado`PreferredWidth` es igual en valor a la corriente`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Sirve como una función hash para este tipo. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Devuelve una cadena fácil de usar que muestra el valor de este objeto. |

## Campos

| Nombre | Descripción |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Devuelve una instancia que representa el valor "no se especifica el ancho preferido". |

## Observaciones

El ancho preferido se puede especificar como un porcentaje, número de puntos o un valor especial "ninguno/automático".

Las instancias de esta clase son inmutables.

## Ejemplos

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

* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)
