---
title: ImageSize Class
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.ImageSize, su recurso ideal para obtener información detallada sobre el tamaño y la resolución de las imágenes para mejorar la calidad de los documentos.
type: docs
weight: 1400
url: /es/net/aspose.words.drawing/imagesize/
---
## ImageSize class

Contiene información sobre el tamaño y la resolución de la imagen.

Para obtener más información, visite el[Trabajar con imágenes](https://docs.aspose.com/words/net/working-with-images/) Artículo de documentación.

```csharp
public class ImageSize
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ImageSize](imagesize/#constructor)(*int, int*) | Inicializa el ancho y la altura a los valores dados en píxeles. Inicializa la resolución a 96 ppp. |
| [ImageSize](imagesize/#constructor_1)(*int, int, double, double*) | Inicializa el ancho, la altura y la resolución a los valores dados. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [HeightPixels](../../aspose.words.drawing/imagesize/heightpixels/) { get; } | Obtiene la altura de la imagen en píxeles. |
| [HeightPoints](../../aspose.words.drawing/imagesize/heightpoints/) { get; } | Obtiene la altura de la imagen en puntos. 1 punto equivale a 1/72 de pulgada. |
| [HorizontalResolution](../../aspose.words.drawing/imagesize/horizontalresolution/) { get; } | Obtiene la resolución horizontal en DPI. |
| [VerticalResolution](../../aspose.words.drawing/imagesize/verticalresolution/) { get; } | Obtiene la resolución vertical en DPI. |
| [WidthPixels](../../aspose.words.drawing/imagesize/widthpixels/) { get; } | Obtiene el ancho de la imagen en píxeles. |
| [WidthPoints](../../aspose.words.drawing/imagesize/widthpoints/) { get; } | Obtiene el ancho de la imagen en puntos. 1 punto equivale a 1/72 de pulgada. |

## Ejemplos

Muestra cómo cambiar el tamaño de una forma con una imagen.

```csharp
// Cuando insertamos una imagen usando el método "InsertImage", el constructor escala la forma que muestra la imagen de modo que,
// cuando vemos el documento usando el zoom del 100% en Microsoft Word, la forma muestra la imagen en su tamaño real.
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Una imagen de 400x400 creará un objeto ImageData con un tamaño de imagen de 300x300pt.
ImageSize imageSize = shape.ImageData.ImageSize;

Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

// Si las dimensiones de una forma coinciden con las dimensiones de los datos de la imagen,
//Entonces la forma muestra la imagen en su tamaño original.
Assert.AreEqual(300.0d, shape.Width);
Assert.AreEqual(300.0d, shape.Height);

 // Reduce el tamaño general de la forma en un 50%.
shape.Width *= 0.5;

 // Los factores de escala se aplican tanto al ancho como a la altura al mismo tiempo para preservar las proporciones de la forma.
Assert.AreEqual(150.0d, shape.Width);
Assert.AreEqual(150.0d, shape.Height);

// Cuando cambiamos el tamaño de la forma, el tamaño de los datos de la imagen permanece igual.
Assert.AreEqual(300.0d, imageSize.WidthPoints);
Assert.AreEqual(300.0d, imageSize.HeightPoints);

//Podemos referenciar las dimensiones de los datos de la imagen para aplicar una escala en función del tamaño de la imagen.
shape.Width = imageSize.WidthPoints * 1.1;

Assert.AreEqual(330.0d, shape.Width);
Assert.AreEqual(330.0d, shape.Height);

doc.Save(ArtifactsDir + "Image.ScaleImage.docx");
```

### Ver también

* property [ImageSize](../imagedata/imagesize/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
