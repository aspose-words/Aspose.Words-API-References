---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsLayoutInCell de ShapeBase, controle la ubicación de formas en las tablas para lograr una mayor flexibilidad de diseño y una mejor gestión del diseño.
type: docs
weight: 330
url: /es/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Obtiene o establece un indicador que indica si la forma se muestra dentro de una tabla o fuera de ella.

```csharp
public bool IsLayoutInCell { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero`.

Tiene efecto solo para formas de nivel superior, la propiedad[`WrapType`](../wraptype/) de los cuales se establece en valor distinto de[`Inline`](../../../aspose.words/inline/).

## Ejemplos

Muestra cómo determinar cómo mostrar una forma en una celda de tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 10;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Single;

table.Style = tableStyle;

builder.MoveTo(table.FirstRow.FirstCell.FirstParagraph);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);

// Establezca la propiedad "IsLayoutInCell" en "true" para mostrar la forma como un elemento en línea dentro del párrafo de la celda.
// El origen de coordenadas que determinará la ubicación de la forma será la esquina superior izquierda de la celda de la forma.
// Si redimensionamos la celda, la forma se moverá para mantener la misma posición comenzando desde la parte superior izquierda de la celda.
// Establezca la propiedad "IsLayoutInCell" en "falso" para mostrar la forma como una forma flotante independiente.
//El origen de coordenadas que determinará la ubicación de la forma será la esquina superior izquierda de la página,
// y la forma no responderá a ningún cambio de tamaño de su celda.
shape.IsLayoutInCell = isLayoutInCell;

//Solo podemos aplicar la propiedad "IsLayoutInCell" a formas flotantes.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
