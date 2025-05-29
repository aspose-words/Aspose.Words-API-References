---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words para .NET
description: Agrupe formas fácilmente con el método InsertGroupShape de DocumentBuilder. Cree diseños organizados insertando nuevos nodos GroupShape sin problemas.
type: docs
weight: 360
url: /es/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape que se inserta en la posición actual.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| shapes | ShapeBase[] | La lista de formas que se agruparán. |

## Observaciones

La posición y la dimensión del nuevo GroupShape se calcularán automáticamente.

Las formas VML y DML no se pueden agrupar.

## Ejemplos

Muestra cómo combinar la forma del grupo con la forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Combina formas en un nodo GroupShape que se inserta en la posición especificada.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// Combine los nodos Shape y GroupShape.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

Muestra cómo insertar una forma de grupo DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Dimensiones para el nuevo nodo GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Inserte el nodo GroupShape para el tamaño especificado que se inserta en la posición especificada.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Inserte el nodo GroupShape cuya posición y dimensión se calcularán automáticamente.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Ver también

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape del tamaño especificado que se inserta en la posición especificada.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la forma del grupo. |
| top | Double | Distancia en puntos desde el origen hasta el lado superior de la forma del grupo. |
| width | Double | Ancho de la forma del grupo en puntos. No se permiten valores negativos. |
| height | Double | Altura de la forma del grupo en puntos. No se permiten valores negativos. |
| shapes | ShapeBase[] | La lista de formas que se agruparán. |

## Observaciones

Las formas VML y DML no se pueden agrupar.

## Ejemplos

Muestra cómo insertar una forma de grupo DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Dimensiones para el nuevo nodo GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Inserte el nodo GroupShape para el tamaño especificado que se inserta en la posición especificada.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Inserte el nodo GroupShape cuya posición y dimensión se calcularán automáticamente.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Ver también

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
