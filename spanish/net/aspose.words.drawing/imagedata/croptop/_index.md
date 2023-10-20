---
title: ImageData.CropTop
linktitle: CropTop
articleTitle: CropTop
second_title: Aspose.Words para .NET
description: ImageData CropTop propiedad. Define la fracción de eliminación de la imagen desde la parte superior en C#.
type: docs
weight: 90
url: /es/net/aspose.words.drawing/imagedata/croptop/
---
## ImageData.CropTop property

Define la fracción de eliminación de la imagen desde la parte superior.

```csharp
public double CropTop { get; set; }
```

## Observaciones

La cantidad de recorte puede oscilar entre -1,0 y 1,0. El valor predeterminado es 0. Tenga en cuenta que un valor de 1 no mostrará ninguna imagen. Los valores negativos darán como resultado que la imagen se comprima hacia adentro desde el borde que se está recortando (el espacio vacío entre la imagen y el borde recortado se llenará con el color de relleno de la forma ). Los valores positivos inferiores a 1 darán como resultado que la imagen restante se estire para ajustarse a la forma.

El valor predeterminado es 0.

## Ejemplos

Muestra cómo editar los datos de imagen de una forma.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Importa una forma del documento fuente y añádela al primer párrafo.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// La forma importada contiene una imagen. Podemos acceder a las propiedades de la imagen y a los datos sin procesar a través del objeto ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Si una imagen no tiene bordes, su objeto ImageData definirá el color del borde como vacío.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Esta imagen no se vincula a otra forma o archivo de imagen en el sistema de archivos local.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Las propiedades "Brillo" y "Contraste" definen el brillo y el contraste de la imagen
// en una escala de 0 a 1, con el valor predeterminado de 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Los valores de brillo y contraste anteriores han creado una imagen con mucho blanco.
// Podemos seleccionar un color con la propiedad ChromaKey para reemplazarlo con transparencia, como por ejemplo el blanco.
imageData.ChromaKey = Color.White;

// Importa la forma de origen nuevamente y configura la imagen en monocromática.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importa la forma de origen nuevamente para crear una tercera imagen y configúrala en BiLevel.
// BiLevel establece cada píxel en blanco o negro, el que esté más cerca del color original.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// El recorte se determina en una escala de 0-1. Recortar un lado en 0,3
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
