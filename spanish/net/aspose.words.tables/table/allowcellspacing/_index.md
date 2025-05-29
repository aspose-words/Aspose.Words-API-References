---
title: Table.AllowCellSpacing
linktitle: AllowCellSpacing
articleTitle: AllowCellSpacing
second_title: Aspose.Words para .NET
description: Descubre la propiedad "AllowCellSpacing" de la tabla para gestionar fácilmente el espaciado entre celdas en tus diseños. ¡Mejora tu diseño con opciones personalizables!
type: docs
weight: 60
url: /es/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Obtiene o establece la opción "Permitir espaciado entre celdas".

```csharp
public bool AllowCellSpacing { get; set; }
```

## Ejemplos

Muestra cómo habilitar el espaciado entre celdas individuales en una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Animal");
builder.InsertCell();
builder.Write("Class");
builder.EndRow();
builder.InsertCell();
builder.Write("Dog");
builder.InsertCell();
builder.Write("Mammal");
builder.EndTable();

table.CellSpacing = 3;

// Establezca la propiedad "AllowCellSpacing" en "verdadero" para habilitar el espaciado entre celdas
// con una magnitud igual al valor de la propiedad "CellSpacing", en puntos.
// Establezca la propiedad "AllowCellSpacing" en "false" para deshabilitar el espaciado entre celdas
// e ignorar el valor de la propiedad "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Al ajustar la propiedad "CellSpacing" se habilitará automáticamente el espaciado de celdas.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
