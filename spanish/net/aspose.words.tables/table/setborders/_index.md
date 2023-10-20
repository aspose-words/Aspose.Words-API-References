---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: Aspose.Words para .NET
description: Table SetBorders método. Establece todos los bordes de la tabla con el estilo ancho y color de línea especificados en C#.
type: docs
weight: 420
url: /es/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Establece todos los bordes de la tabla con el estilo, ancho y color de línea especificados.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| lineStyle | LineStyle | El estilo de línea que se aplicará. |
| lineWidth | Double | El ancho de línea a establecer (en puntos). |
| color | Color | El color que se utilizará para el borde. |

## Ejemplos

Muestra cómo formatear todos los bordes de una tabla a la vez.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Borra todos los bordes existentes de la tabla.
table.ClearBorders();

// Establece una única línea verde para que sirva como cada borde exterior e interior de esta tabla.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Muestra cómo aplicar colores de borde y sombreado mientras construye una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inicia una tabla y establece un color/grosor predeterminado para sus bordes.
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

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
