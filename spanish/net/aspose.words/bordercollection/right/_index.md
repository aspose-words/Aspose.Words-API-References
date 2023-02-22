---
title: BorderCollection.Right
second_title: Referencia de API de Aspose.Words para .NET
description: BorderCollection propiedad. Obtiene el borde derecho.
type: docs
weight: 100
url: /es/net/aspose.words/bordercollection/right/
---
## BorderCollection.Right property

Obtiene el borde derecho.

```csharp
public Border Right { get; }
```

### Ejemplos

Muestra cómo aplicar borde y color de sombreado al crear una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inicie una tabla y establezca un color/grosor predeterminado para sus bordes.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Crea una fila con dos celdas con diferentes colores de fondo.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Restablece el formato de celda para deshabilitar los colores de fondo
// establece un grosor de borde personalizado para todas las celdas nuevas creadas por el constructor,
// luego construye una segunda fila.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Ver también

* class [Border](../../border/)
* class [BorderCollection](../)
* espacio de nombres [Aspose.Words](../../bordercollection/)
* asamblea [Aspose.Words](../../../)


