---
title: ImageSize.WidthPixels
linktitle: WidthPixels
articleTitle: WidthPixels
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImageSize WidthPixels para recuperar fácilmente el ancho de píxeles de sus imágenes, mejorando la gestión y optimización de sus imágenes.
type: docs
weight: 60
url: /es/net/aspose.words.drawing/imagesize/widthpixels/
---
## ImageSize.WidthPixels property

Obtiene el ancho de la imagen en píxeles.

```csharp
public int WidthPixels { get; }
```

## Ejemplos

Muestra cómo leer las propiedades de una imagen en una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una forma en el documento que contiene una imagen tomada de nuestro sistema de archivos local.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Si la forma contiene una imagen, su propiedad ImageData será válida,
// y contendrá un objeto ImageSize.
ImageSize imageSize = shape.ImageData.ImageSize;

// El objeto ImageSize contiene información de solo lectura sobre la imagen dentro de la forma.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

//Podemos basar el tamaño de la forma en el tamaño de su imagen para evitar estirar la imagen.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Ver también

* class [ImageSize](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
