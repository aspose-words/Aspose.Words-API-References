---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase CanHaveImage : apprenez à déterminer si votre type de forme prend en charge les images pour un attrait visuel amélioré !
type: docs
weight: 100
url: /fr/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Retours`vrai` si le type de forme permet à la forme d'avoir une image.

```csharp
public bool CanHaveImage { get; }
```

## Remarques

Bien que Microsoft Word dispose d'un type de forme spécial pour les images, il semble que dans les documents Microsoft Word, toute forme shape , à l'exception d'une forme de groupe, puisse avoir une image. Par conséquent, cette propriété renvoie`vrai` pour toutes les formes sauf[`GroupShape`](../../groupshape/).

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
