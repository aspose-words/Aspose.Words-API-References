---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words para .NET
description: Descubre la propiedad BorderCollection Horizontal para crear bordes uniformes en celdas y párrafos. ¡Mejora tu diseño con una alineación y un estilo perfectos!
type: docs
weight: 50
url: /es/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Obtiene el borde horizontal que se utiliza entre celdas o párrafos conformes.

```csharp
public Border Horizontal { get; }
```

## Ejemplos

Muestra cómo aplicar configuraciones a los bordes horizontales del formato de un párrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un borde horizontal rojo para el párrafo. Los párrafos creados posteriormente heredarán esta configuración de borde.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Escribe texto en el documento sin crear un nuevo párrafo después.
// Como no hay ningún párrafo debajo, el borde horizontal no será visible.
builder.Write("Paragraph above horizontal border.");

// Una vez que agreguemos un segundo párrafo, el borde del primer párrafo se hará visible.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

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
