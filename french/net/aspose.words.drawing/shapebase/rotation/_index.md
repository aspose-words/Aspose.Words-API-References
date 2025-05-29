---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase Rotation, définissez et personnalisez facilement les angles de rotation de vos formes, améliorant ainsi la précision et la créativité de votre conception.
type: docs
weight: 500
url: /fr/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Définit l'angle (en degrés) selon lequel une forme est tournée. Une valeur positive correspond à un angle de rotation dans le sens des aiguilles d'une montre.

```csharp
public double Rotation { get; set; }
```

## Remarques

La valeur par défaut est 0.

## Exemples

Montre comment insérer et faire pivoter une image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une forme avec une image.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Faites pivoter l'image de 45 degrés dans le sens des aiguilles d'une montre.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
