---
title: TableStyle.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words para .NET
description: Descubre la propiedad TableStyle BottomPadding y personaliza el espaciado entre celdas de tu tabla para mejorar el diseño y la legibilidad. ¡Optimiza tu diseño fácilmente!
type: docs
weight: 50
url: /es/net/aspose.words/tablestyle/bottompadding/
---
## TableStyle.BottomPadding property

Obtiene o establece la cantidad de espacio (en puntos) que se agregará debajo del contenido de las celdas de la tabla.

```csharp
public double BottomPadding { get; set; }
```

## Ejemplos

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

* class [TableStyle](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
