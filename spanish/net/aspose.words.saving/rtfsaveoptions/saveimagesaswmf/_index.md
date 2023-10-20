---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words para .NET
description: RtfSaveOptions SaveImagesAsWmf propiedad. cuandoverdadero todas las imágenes se guardarán como WMF en C#.
type: docs
weight: 50
url: /es/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

cuando`verdadero` todas las imágenes se guardarán como WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## Observaciones

Esta opción puede ayudar a evitar mensajes de advertencia de WordPad.

## Ejemplos

Muestra cómo convertir todas las imágenes de un documento al formato Metarchivo de Windows mientras guardamos el documento como RTF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.AreEqual(ImageType.Jpeg, imageShape.ImageData.ImageType);

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ImageType.Png, imageShape.ImageData.ImageType);

// Crea un objeto "RtfSaveOptions" para pasarlo al método "Guardar" del documento para modificar cómo lo guardamos en un RTF.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Establezca la propiedad "SaveImagesAsWmf" en "true" para convertir todas las imágenes del documento a WMF a medida que lo guardamos en RTF.
// Hacerlo ayudará a lectores como WordPad a leer nuestro documento.
// Establece la propiedad "SaveImagesAsWmf" en "false" para conservar el formato original de todas las imágenes del documento
// mientras lo guardamos en RTF. Esto preservará la calidad de las imágenes a costa de la compatibilidad con lectores RTF más antiguos.
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[1]).ImageData.ImageType);
}
else
{
    Assert.AreEqual(ImageType.Jpeg, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Png, ((Shape)shapes[1]).ImageData.ImageType);
}
```

### Ver también

* class [RtfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
