---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageWidth de PageSetup para ajustar fácilmente el ancho de página en puntos, mejorando el diseño de su documento para una presentación óptima.
type: docs
weight: 340
url: /es/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

Devuelve o establece el ancho de la página en puntos.

```csharp
public double PageWidth { get; set; }
```

## Ejemplos

Muestra cómo insertar una imagen y usarla como marca de agua.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta la imagen en el encabezado para que sea visible en todas las páginas.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

//Coloca la imagen en el centro de la página.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

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

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
