---
title: ImageSize.VerticalResolution
linktitle: VerticalResolution
articleTitle: VerticalResolution
second_title: Aspose.Words pour .NET
description: ImageSize VerticalResolution propriété. Obtient la résolution verticale en DPI en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing/imagesize/verticalresolution/
---
## ImageSize.VerticalResolution property

Obtient la résolution verticale en DPI.

```csharp
public double VerticalResolution { get; }
```

## Exemples

Montre comment lire les propriétés d’une image dans une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère une forme dans le document qui contient une image extraite de notre système de fichiers local.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Si la forme contient une image, sa propriété ImageData sera valide,
// et il contiendra un objet ImageSize.
ImageSize imageSize = shape.ImageData.ImageSize; 

// L'objet ImageSize contient des informations en lecture seule sur l'image dans la forme.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// On peut baser la taille de la forme sur la taille de son image pour éviter d'étirer l'image.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Voir également

* class [ImageSize](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
