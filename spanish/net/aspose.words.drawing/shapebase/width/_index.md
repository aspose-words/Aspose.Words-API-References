---
title: ShapeBase.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words para .NET
description: ShapeBase Width propiedad. Obtiene o establece el ancho del bloque contenedor de la forma en C#.
type: docs
weight: 570
url: /es/net/aspose.words.drawing/shapebase/width/
---
## ShapeBase.Width property

Obtiene o establece el ancho del bloque contenedor de la forma.

```csharp
public double Width { get; set; }
```

## Observaciones

Para una forma de nivel superior, el valor está en puntos.

Para formas en un grupo, el valor está en el espacio de coordenadas y las unidades del grupo principal.

El valor predeterminado es 0.

## Ejemplos

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

Muestra cómo cambiar el tamaño de una forma con una imagen.

```csharp
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            // Cuando insertamos una imagen usando el método "InsertImage", el constructor escala la forma que muestra la imagen para que,
            // cuando vemos el documento usando un zoom del 100% en Microsoft Word, la forma muestra la imagen en su tamaño real.
            Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);
            Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

            // Una imagen de 400x400 creará un objeto ImageData con un tamaño de imagen de 300x300pt.
            ImageSize imageSize = shape.ImageData.ImageSize;

            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Si las dimensiones de una forma coinciden con las dimensiones de los datos de la imagen,
            // entonces la forma muestra la imagen en su tamaño original.
            Assert.AreEqual(300.0d, shape.Width);
            Assert.AreEqual(300.0d, shape.Height);

             // Reducir el tamaño total de la forma en un 50%.
            shape.Width *= 0.5;

             // Los factores de escala se aplican tanto al ancho como al alto al mismo tiempo para preservar las proporciones de la forma.
            Assert.AreEqual(150.0d, shape.Width);
            Assert.AreEqual(150.0d, shape.Height);

            // Cuando cambiamos el tamaño de la forma, el tamaño de los datos de la imagen sigue siendo el mismo.
            Assert.AreEqual(300.0d, imageSize.WidthPoints);
            Assert.AreEqual(300.0d, imageSize.HeightPoints);

            // Podemos hacer referencia a las dimensiones de los datos de la imagen para aplicar una escala basada en el tamaño de la imagen.
            shape.Width = imageSize.WidthPoints * 1.1;

            Assert.AreEqual(330.0d, shape.Width);
            Assert.AreEqual(330.0d, shape.Height);

            doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
