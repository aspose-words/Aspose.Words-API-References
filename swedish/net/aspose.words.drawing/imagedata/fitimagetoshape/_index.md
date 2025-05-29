---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words för .NET
description: Optimera dina bilder med metoden FitImageToShape, vilket säkerställer perfekt bildförhållandejustering inom formramar för fantastiska visuella presentationer.
type: docs
weight: 190
url: /sv/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Anpassar bilddata till formramen så att bilddatans bildförhållande matchar formramens bildförhållande.

```csharp
public void FitImageToShape()
```

## Exempel

Visar hot för att anpassa bilddata till formram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en bildform och lämna dess orientering i standardläget.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
