---
title: ShapeBase.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words para .NET
description: Descubre la propiedad ShapeBase Left para ajustar fácilmente la posición del borde izquierdo de tu forma dentro de su contenedor. ¡Mejora la precisión de tus diseños hoy mismo!
type: docs
weight: 390
url: /es/net/aspose.words.drawing/shapebase/left/
---
## ShapeBase.Left property

Obtiene o establece la posición del borde izquierdo del bloque contenedor de la forma.

```csharp
public double Left { get; set; }
```

## Observaciones

Para una forma de nivel superior, el valor está en puntos y es relativo al ancla de la forma.

Para las formas de un grupo, el valor está en el espacio de coordenadas y las unidades del grupo principal.

El valor predeterminado es 0.

Tiene efecto sólo para formas flotantes.

## Ejemplos

Muestra cómo insertar una imagen flotante y especificar su posición y tamaño.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configure la propiedad "RelativeHorizontalPosition" de la forma para tratar el valor de la propiedad "Left"
 // como la distancia horizontal de la forma, en puntos, desde el lado izquierdo de la página.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Establezca la distancia horizontal de la forma desde el lado izquierdo de la página en 100.
shape.Left = 100;

// Utilice la propiedad "RelativeVerticalPosition" de manera similar para posicionar la forma 80 puntos debajo de la parte superior de la página.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Establezca la altura de la forma, que escalará automáticamente el ancho para preservar las dimensiones.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Las propiedades "Abajo" y "Derecha" contienen los bordes inferior y derecho de la imagen.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
