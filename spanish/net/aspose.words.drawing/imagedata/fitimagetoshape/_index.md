---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words para .NET
description: Optimice sus imágenes con el método FitImageToShape, asegurando una alineación perfecta de la relación de aspecto dentro de los marcos de forma para lograr presentaciones visuales impresionantes.
type: docs
weight: 190
url: /es/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Ajusta los datos de la imagen al marco de forma para que la relación de aspecto de los datos de la imagen coincida con la relación de aspecto del marco de forma.

```csharp
public void FitImageToShape()
```

## Ejemplos

Muestra cómo ajustar los datos de la imagen al marco de forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una forma de imagen y deja su orientación en su estado predeterminado.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
