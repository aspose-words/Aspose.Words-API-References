---
title: Cell.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words para .NET
description: Descubra la propiedad LastParagraph de la celda. Acceda fácilmente al último párrafo desde los elementos secundarios inmediatos para una gestión eficiente del contenido.
type: docs
weight: 60
url: /es/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

Obtiene el último párrafo entre los hijos inmediatos.

```csharp
public Paragraph LastParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
