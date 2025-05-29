---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase AspectRatioLocked pour conserver facilement les proportions de vos formes et créer des designs parfaits. Optimisez vos projets dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Spécifie si le rapport hauteur/largeur de la forme est verrouillé.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Remarques

La valeur par défaut dépend de la[`ShapeType`](../../shapetype/) , pour leImage c'est`vrai` mais pour les autres types de formes, c'est`FAUX`.

N'a d'effet que sur les formes de niveau supérieur.

## Exemples

Montre comment verrouiller/déverrouiller le rapport hauteur/largeur d'une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer une forme. Si nous ouvrons ce document dans Microsoft Word, nous pouvons faire un clic gauche sur la forme pour l'afficher.
// huit poignées de dimensionnement autour de son périmètre, sur lesquelles nous pouvons cliquer et faire glisser pour modifier sa taille.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Définissez la propriété « AspectRatioLocked » sur « true » pour préserver le rapport hauteur/largeur de la forme
// lors de l'utilisation de l'une des quatre poignées de dimensionnement diagonales, qui modifient à la fois la hauteur et la largeur de l'image.
// L'utilisation de poignées de dimensionnement orthogonales qui modifient la hauteur ou la largeur modifiera toujours le rapport hauteur/largeur.
// Définissez la propriété « AspectRatioLocked » sur « false » pour nous permettre de
// modifiez librement le rapport hauteur/largeur de l'image avec toutes les poignées de dimensionnement.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
