---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words for .NET
description: ImageData FitImageToShape method. Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame in C#.
type: docs
weight: 190
url: /net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Fits the image data to Shape frame so that the aspect ratio of the image data matches the aspect ratio of Shape frame.

```csharp
public void FitImageToShape()
```

## Examples

Shows hot to fit the image data to Shape frame.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert an image shape and leave its orientation in its default state.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
