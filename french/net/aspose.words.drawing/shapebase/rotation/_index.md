---
title: ShapeBase.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words pour .NET
description: ShapeBase Rotation propriété. Définit langle en degrés de rotation dune forme. La valeur positive correspond à langle de rotation dans le sens des aiguilles dune montre en C#.
type: docs
weight: 470
url: /fr/net/aspose.words.drawing/shapebase/rotation/
---
## ShapeBase.Rotation property

Définit l'angle (en degrés) de rotation d'une forme. La valeur positive correspond à l'angle de rotation dans le sens des aiguilles d'une montre.

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

// Insère une forme avec une image.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
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
