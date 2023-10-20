---
title: Table.CellSpacing
linktitle: CellSpacing
articleTitle: CellSpacing
second_title: Aspose.Words para .NET
description: Table CellSpacing propiedad. Obtiene o establece la cantidad de espacio en puntos entre las celdas en C#.
type: docs
weight: 100
url: /es/net/aspose.words.tables/table/cellspacing/
---
## Table.CellSpacing property

Obtiene o establece la cantidad de espacio (en puntos) entre las celdas.

```csharp
public double CellSpacing { get; set; }
```

## Ejemplos

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

Muestra cómo crear configuraciones de estilo personalizadas para la tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Name");
builder.InsertCell();
builder.Write("مرحبًا");
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.AllowBreakAcrossPages = true;
tableStyle.Bidi = true;
tableStyle.CellSpacing = 5;
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 5;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;
tableStyle.VerticalAlignment = CellVerticalAlignment.Center;

table.Style = tableStyle;

// Establecer las propiedades de estilo de una tabla puede afectar las propiedades de la tabla misma.
Assert.True(table.Bidi);
Assert.AreEqual(5.0d, table.CellSpacing);
Assert.AreEqual("MyTableStyle1", table.StyleName);

doc.Save(ArtifactsDir + "Table.TableStyleCreation.docx");
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
