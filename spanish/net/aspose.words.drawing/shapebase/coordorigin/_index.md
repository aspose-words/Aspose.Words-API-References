---
title: ShapeBase.CoordOrigin
linktitle: CoordOrigin
articleTitle: CoordOrigin
second_title: Aspose.Words para .NET
description: Descubre la propiedad ShapeBase CoordOrigin para optimizar tus diseños. Accede a las coordenadas precisas de la esquina superior izquierda del bloque contenedor de tu forma.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Las coordenadas en la esquina superior izquierda del bloque que contiene esta forma.

```csharp
public Point CoordOrigin { get; set; }
```

## Observaciones

El valor predeterminado es (0,0).

## Ejemplos

Muestra cómo traducir la ubicación de las coordenadas x e y en el plano de coordenadas de una forma a una ubicación en el plano de coordenadas de la forma principal.

```csharp
Document doc = new Document();

// Inserta una forma de grupo y colócala 100 puntos debajo y a la derecha de
// el punto de origen de las coordenadas x e y del documento.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Utilice el método "LocalToParent" para determinar que (0, 0) en las coordenadas x e y internas del grupo
// se encuentra en (100, 100) del sistema de coordenadas de su forma padre. El padre de la forma del grupo es el propio documento.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// De forma predeterminada, el plano de coordenadas interno de una forma tiene la esquina superior izquierda en (0, 0),
// y la esquina inferior derecha en (1000, 1000). Debido a su tamaño, nuestra forma de grupo cubre un área de 500 × 500 puntos.
// en el plano del documento. Esto significa que un movimiento de 1 punto en el plano de coordenadas del documento se traducirá
// a un movimiento de 2 puntos en el plano de coordenadas de la forma del grupo.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Mueva el origen de los ejes x e y de la forma del grupo desde la esquina superior izquierda al centro.
// Esto desplazará aún más las coordenadas internas del grupo con respecto a las coordenadas del documento.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Cambiar la escala del plano de coordenadas también afectará las ubicaciones relativas.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Si deseamos agregar una forma a este grupo mientras definimos su ubicación en función de una ubicación en el documento,
// Primero necesitaremos confirmar una ubicación en la forma del grupo que coincida con la ubicación del documento.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

Muestra cómo crear y rellenar una forma de grupo.

```csharp
Document doc = new Document();

// Crear una forma de grupo. Una forma de grupo puede mostrar una colección de nodos de forma secundarios.
// En Microsoft Word, al hacer clic dentro del límite de la forma del grupo o en una de las formas secundarias de la forma del grupo,
// selecciona todas las demás formas secundarias dentro de este grupo y nos permite escalar y mover todas las formas a la vez.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Cree una forma de grupo de 400pt x 400pt y colóquela en el origen de coordenadas de la forma flotante del documento.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Establezca el tamaño del plano de coordenadas interno del grupo en 500 x 500 puntos.
// La esquina superior izquierda del grupo tendrá una coordenada x e y de (0, 0),
// y la esquina inferior derecha tendrá una coordenada x e y de (500, 500).
group.CoordSize = new Size(500, 500);

 // Establezca las coordenadas de la esquina superior izquierda del grupo en (-250, -250).
// El centro del grupo ahora tendrá un valor de coordenadas x e y de (0, 0),
// y la esquina inferior derecha estará en (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Cree un rectángulo que mostrará el límite de esta forma de grupo y agréguelo al grupo.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// Una vez que una forma es parte de un grupo de formas, podemos acceder a ella como un nodo secundario y luego modificarla.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Crea una pequeña estrella roja e insértala en el grupo.
// Alinea la forma con el origen de coordenadas del grupo, que hemos movido al centro.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// Inserta un rectángulo y luego inserta un rectángulo ligeramente más pequeño en el mismo lugar con una imagen.
Las formas nuevas que añadimos al grupo se superponen a las antiguas. El rectángulo azul claro se superpondrá parcialmente a la estrella roja.
// y luego la forma con la imagen se superpondrá al rectángulo azul claro, usándolo como marco.
// No podemos utilizar las propiedades "ZOrder" de las formas para manipular su disposición dentro de una forma de grupo.
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Insertar un cuadro de texto en la forma del grupo. Configurar la propiedad "Izquierda" para que el borde derecho del cuadro de texto...
// toca el límite derecho de la forma del grupo. Establezca la propiedad "Superior" para que el cuadro de texto quede fuera.
// el límite de la forma del grupo, con su tamaño superior alineado a lo largo del margen inferior de la forma del grupo.
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
