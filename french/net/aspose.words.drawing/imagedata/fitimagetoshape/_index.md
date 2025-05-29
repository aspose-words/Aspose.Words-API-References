---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words pour .NET
description: Optimisez vos images avec la méthode FitImageToShape, garantissant un alignement parfait des proportions dans les cadres Shape pour des présentations visuelles époustouflantes.
type: docs
weight: 190
url: /fr/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Ajuste les données d'image au cadre de forme afin que le rapport hauteur/largeur des données d'image corresponde au rapport hauteur/largeur du cadre de forme.

```csharp
public void FitImageToShape()
```

## Exemples

Affiche la procédure à suivre pour adapter les données de l'image au cadre de forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une forme d'image et laissez son orientation dans son état par défaut.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### Voir également

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
