---
title: ImageSaveOptions.ImageSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: ImageSaveOptions constructor. Inicializa una nueva instancia de esta clase que se puede usar para guardar imágenes renderizadas en Tiff Png Bmp  Jpeg Emf Eps oSvg formato.
type: docs
weight: 10
url: /es/net/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions constructor

Inicializa una nueva instancia de esta clase que se puede usar para guardar imágenes renderizadas en Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps oSvg formato.

```csharp
public ImageSaveOptions(SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| saveFormat | SaveFormat | Puede ser Tiff ,Png ,Bmp , Jpeg ,Emf ,Eps oSvg formato. |

### Ejemplos

Muestra cómo configurar la compresión al guardar un documento como JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);

// Establece la propiedad "JpegQuality" en "10" para utilizar una compresión más fuerte al renderizar el documento.
// Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más destacados.
imageOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg").Length));

// Establece la propiedad "JpegQuality" en "100" para utilizar una compresión más débil al renderizar el documento.
// Esto mejorará la calidad de la imagen a costa de un mayor tamaño de archivo.
imageOptions.JpegQuality = 100;

doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

Assert.That(60000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg").Length));
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../imagesaveoptions/)
* asamblea [Aspose.Words](../../../)


