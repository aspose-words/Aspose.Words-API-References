---
title: ShapeBase.Bottom
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase propiedad. Obtiene la posición del borde inferior del bloque contenedor de la forma.
type: docs
weight: 60
url: /es/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

Obtiene la posición del borde inferior del bloque contenedor de la forma.

```csharp
public double Bottom { get; }
```

### Observaciones

Para una forma de nivel superior, el valor está en puntos y es relativo al anclaje de la forma.

Para formas en un grupo, el valor está en el espacio de coordenadas y las unidades del grupo principal.

### Ejemplos

Muestra cómo insertar una imagen flotante y especificar su posición y tamaño.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configura la propiedad "RelativeHorizontalPosition" de la forma para tratar el valor de la propiedad "Left"
 // como la distancia horizontal de la forma, en puntos, desde el lado izquierdo de la página.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Establece la distancia horizontal de la forma desde el lado izquierdo de la página a 100.
shape.Left = 100;

// Utilice la propiedad "RelativeVerticalPosition" de manera similar para colocar la forma 80 puntos debajo de la parte superior de la página.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Establece la altura de la forma, que escalará automáticamente el ancho para preservar las dimensiones.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Las propiedades "Inferior" y "Derecha" contienen los bordes inferior y derecho de la imagen.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


