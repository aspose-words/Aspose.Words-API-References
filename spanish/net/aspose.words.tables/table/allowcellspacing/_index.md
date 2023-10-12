---
title: Table.AllowCellSpacing
second_title: Referencia de API de Aspose.Words para .NET
description: Table propiedad. Obtiene o establece la opción Permitir espacio entre celdas.
type: docs
weight: 60
url: /es/net/aspose.words.tables/table/allowcellspacing/
---
## Table.AllowCellSpacing property

Obtiene o establece la opción "Permitir espacio entre celdas".

```csharp
public bool AllowCellSpacing { get; set; }
```

### Ejemplos

Muestra cómo habilitar el espacio entre celdas individuales en una tabla.

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

// Establece la propiedad "AllowCellSpacing" en "true" para habilitar el espacio entre celdas
// con una magnitud igual al valor de la propiedad "CellSpacing", en puntos.
// Establece la propiedad "AllowCellSpacing" en "false" para deshabilitar el espaciado de celdas
// e ignorar el valor de la propiedad "CellSpacing".
table.AllowCellSpacing = allowCellSpacing;

doc.Save(ArtifactsDir + "Table.AllowCellSpacing.html");

// Ajustar la propiedad "CellSpacing" habilitará automáticamente el espaciado de celdas.
table.CellSpacing = 5;

Assert.True(table.AllowCellSpacing);
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../table/)
* asamblea [Aspose.Words](../../../)


