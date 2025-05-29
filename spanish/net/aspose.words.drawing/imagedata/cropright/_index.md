---
title: ImageData.CropRight
linktitle: CropRight
articleTitle: CropRight
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImageData CropRight, controle el recorte de imágenes desde el lado derecho para una edición precisa de la imagen y un atractivo visual mejorado.
type: docs
weight: 80
url: /es/net/aspose.words.drawing/imagedata/cropright/
---
## ImageData.CropRight property

Define la fracción de eliminación de imagen del lado derecho.

```csharp
public double CropRight { get; set; }
```

## Observaciones

El grado de recorte puede variar de -1.0 a 1.0. El valor predeterminado es 0. Tenga en cuenta que un valor de 1 no mostrará ninguna imagen. Los valores negativos harán que la imagen se reduzca hacia adentro desde el borde recortado (el espacio vacío entre la imagen y el borde recortado se rellenará con el color de relleno de la forma). Los valores positivos menores de 1 harán que la imagen restante se estire para ajustarse a la forma.

El valor predeterminado es 0.

## Ejemplos

Muestra cómo editar los datos de imagen de una forma.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Importa una forma del documento de origen y añádela al primer párrafo.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

La forma importada contiene una imagen. Podemos acceder a las propiedades y datos sin procesar de la imagen mediante el objeto ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Si una imagen no tiene bordes, su objeto ImageData definirá el color del borde como vacío.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Esta imagen no se vincula a otro archivo de forma o imagen en el sistema de archivos local.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Las propiedades "Brillo" y "Contraste" definen el brillo y el contraste de la imagen.
// en una escala de 0 a 1, con el valor predeterminado en 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Los valores de brillo y contraste anteriores han creado una imagen con mucho blanco.
//Podemos seleccionar un color con la propiedad ChromaKey para reemplazar con transparencia, como el blanco.
imageData.ChromaKey = Color.White;

// Importe nuevamente la forma de origen y configure la imagen en monocromática.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importe la forma de origen nuevamente para crear una tercera imagen y configúrela en BiLevel.
// BiLevel establece cada píxel en negro o blanco, lo que esté más cerca del color original.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

El recorte se determina en una escala de 0 a 1. Recortar un lado por 0,3
// recortará el 30% de la imagen en el lado recortado.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
