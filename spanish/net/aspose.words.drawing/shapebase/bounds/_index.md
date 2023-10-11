---
title: ShapeBase.Bounds
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Obtiene o establece la ubicación y el tamaño del bloque contenedor de la forma.
type: docs
weight: 70
url: /es/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Obtiene o establece la ubicación y el tamaño del bloque contenedor de la forma.

```csharp
public RectangleF Bounds { get; set; }
```

### Observaciones

Ignora el bloqueo de la relación de aspecto al realizar la configuración.

Para una forma de nivel superior, el valor está en puntos y es relativo al anclaje de la forma.

Para formas en un grupo, el valor está en el espacio de coordenadas y las unidades del grupo principal.

### Ejemplos

Muestra cómo verificar la forma que contiene límites de bloque.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Aunque la línea en sí ocupa poco espacio en la página del documento,
// ocupa un bloque contenedor rectangular, cuyo tamaño podemos determinar usando las propiedades "Límites".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Crea una forma de grupo y luego establece el tamaño del bloque que lo contiene usando la propiedad "Límites".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Crea un rectángulo, verifica el tamaño de su bloque delimitador y luego agrégalo a la forma del grupo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// El plano de coordenadas de la forma del grupo tiene su origen en la esquina superior izquierda del bloque que lo contiene,
// y las coordenadas xey de (1000, 1000) en la esquina inferior derecha.
// La forma de nuestro grupo tiene un tamaño de 250x250 puntos, por lo que cada 4 puntos en el plano de coordenadas de la forma del grupo
// se traduce en 1 punto en el plano de coordenadas del cuerpo del documento.
// Cada forma que insertemos también reducirá su tamaño en un factor de 4.
// El cambio en la propiedad "BoundsInPoints" de la forma reflejará esto.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Inserta una forma y colócala fuera de los límites del bloque contenedor de la forma del grupo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// La huella de la forma del grupo en el cuerpo del documento ha aumentado, pero el bloque contenedor sigue siendo el mismo.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

Muestra cómo crear y rellenar una forma de grupo.

```csharp
Document doc = new Document();

// Crea una forma de grupo. Una forma de grupo puede mostrar una colección de nodos de formas secundarias.
// En Microsoft Word, al hacer clic dentro de los límites de la forma del grupo o en una de las formas secundarias de la forma del grupo,
// selecciona todas las demás formas secundarias dentro de este grupo y nos permite escalar y mover todas las formas a la vez.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Cree una forma de grupo de 400 pt x 400 pt y colóquela en el origen de coordenadas de la forma flotante del documento.
group.Bounds = new RectangleF(0, 0, 400, 400);

// Establece el tamaño del plano de coordenadas interno del grupo en 500 x 500 puntos. 
// La esquina superior izquierda del grupo tendrá una coordenada xey de (0, 0),
// y la esquina inferior derecha tendrá una coordenada xey de (500, 500).
group.CoordSize = new Size(500, 500);

// Establece las coordenadas de la esquina superior izquierda del grupo en (-250, -250). 
// El centro del grupo ahora tendrá un valor de coordenadas xey de (0, 0),
// y la esquina inferior derecha estará en (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Crea un rectángulo que mostrará el límite de esta forma de grupo y agrégalo al grupo.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Una vez que una forma forma parte de una forma de grupo, podemos acceder a ella como un nodo secundario y luego modificarla.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Crea una pequeña estrella roja e insértala en el grupo.
// Alinea la forma con el origen de coordenadas del grupo, que hemos movido al centro.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// Inserta un rectángulo y luego inserta un rectángulo un poco más pequeño en el mismo lugar con una imagen. 
// Las formas más nuevas que agregamos al grupo se superponen a las formas más antiguas. El rectángulo azul claro se superpondrá parcialmente a la estrella roja,
// y luego la forma con la imagen se superpondrá al rectángulo azul claro, usándolo como marco.
// No podemos usar las propiedades "ZOrder" de las formas para manipular su disposición dentro de una forma de grupo. 
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Inserta un cuadro de texto en la forma del grupo. Establezca la propiedad "Izquierda" para que el borde derecho del cuadro de texto
// toca el límite derecho de la forma del grupo. Establezca la propiedad "Superior" para que el cuadro de texto quede afuera
// el límite de la forma del grupo, con su tamaño superior alineado a lo largo del margen inferior de la forma del grupo.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


