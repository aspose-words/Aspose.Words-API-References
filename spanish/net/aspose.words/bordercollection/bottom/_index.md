---
title: BorderCollection.Bottom
linktitle: Bottom
articleTitle: Bottom
second_title: Aspose.Words para .NET
description: Descubra la propiedad BorderCollection Bottom para acceder y personalizar fácilmente su borde inferior para obtener una mayor flexibilidad y estilo de diseño.
type: docs
weight: 10
url: /es/net/aspose.words/bordercollection/bottom/
---
## BorderCollection.Bottom property

Obtiene el borde inferior.

```csharp
public Border Bottom { get; }
```

## Ejemplos

Muestra cómo aplicar colores de borde y sombreado al crear una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inicia una tabla y establece un color y grosor predeterminado para sus bordes.
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

// Restablecer el formato de celda para deshabilitar los colores de fondo
// Establezca un grosor de borde personalizado para todas las celdas nuevas creadas por el generador,
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
