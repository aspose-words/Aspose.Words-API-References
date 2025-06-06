---
title: BorderCollection.Vertical
linktitle: Vertical
articleTitle: Vertical
second_title: Aspose.Words para .NET
description: Descubre la propiedad BorderCollection Vertical para crear bordes de celda uniformes. ¡Mejora tu diseño con bordes verticales personalizables para una apariencia impecable!
type: docs
weight: 130
url: /es/net/aspose.words/bordercollection/vertical/
---
## BorderCollection.Vertical property

Obtiene el borde vertical que se utiliza entre celdas.

```csharp
public Border Vertical { get; }
```

## Ejemplos

Muestra cómo aplicar configuraciones a los bordes verticales del formato de una fila de tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabla con bordes internos rojos y azules.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    //Ajusta la apariencia de los bordes que aparecerán entre las filas.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    //Ajusta la apariencia de los bordes que aparecerán entre las celdas.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Un formato de fila y un párrafo interno de una celda utilizan configuraciones de borde diferentes.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Ver también

* class [Border](../../border/)
* class [BorderCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
